# Decentralized-Education-Platform
構築WEB3ベースの教育プラットフォームにより、教育者と学習者を直接つなぎ、アクセシビリティを高め、コストを削減します。
# Simulating a Decentralized Education Platform
# NOTE: This is a simplified demonstration using Python to simulate
#       interactions with a blockchain-based system.

class DecentralizedEducationPlatform:
    def __init__(self):
        # Simulating a database of educators and courses
        self.educators = {}
        self.courses = {}
        self.enrollments = []

    def register_educator(self, educator_id, educator_info):
        """Register an educator with their ID and info."""
        self.educators[educator_id] = educator_info
        print(f"Educator {educator_id} registered.")

    def add_course(self, course_id, course_info):
        """Add a course with its ID and info."""
        self.courses[course_id] = course_info
        print(f"Course {course_id} added: {course_info}")

    def list_courses(self):
        """List all available courses."""
        for course_id, course_info in self.courses.items():
            print(f"{course_id}: {course_info}")

    def enroll_student(self, student_id, course_id):
        """Enroll a student in a course."""
        if course_id in self.courses:
            self.enrollments.append((student_id, course_id))
            print(f"Student {student_id} enrolled in course {course_id}.")
        else:
            print(f"Course {course_id} not found.")

# Example usage
platform = DecentralizedEducationPlatform()
platform.register_educator("educator1", {"name": "Alice", "subject": "Mathematics"})
platform.add_course("course1", {"title": "Introduction to Algebra", "educator": "educator1"})
platform.list_courses()
platform.enroll_student("student1", "course1")
