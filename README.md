# Test
My First Repository, for learning GitHub.


import json
import csv

def readJson(path):
    '''读入json'''
    content = []
    with open(path, encoding='utf-8')as f:
        content = json.load(f)
    return content

def writeJson(path, content):
    '''写入json'''
    with open(path, 'w', encoding='utf-8')as f:
        json.dump(content, f, indent=4, ensure_ascii=False)

def readCsv(path):
    '''读入csv'''
    with open(path, encoding='utf-8')as f:
        reader = csv.reader(f)
        content = []
        for r in reader:
            content.append(r)
        return content

def writeCsv(path, content):
    '''写入csv'''
    with open(path, 'w', encoding='utf-8',newline = '')as f:
        writer = csv.writer(f)
        for r in content:
            writer.writerow(r)

if __name__ == "__main__":
    #originalJsonPath = r"D:\UnityProjects\demo\Common\Config\Instance\SceneObject\999OutSide.json.txt"
    #originalJsonContent = readJson(originalJsonPath)
    #print(originalJsonPath.split("\\")[-1])
    #writeJson(str(originalJsonPath.split("\\")[-1]), originalJsonContent)

    #originalCsvPath = r"D:\UnityProjects\demo\Common\Config\Item.csv"
    #originalCsvContent = readCsv(originalCsvPath)
    #writeCsv(originalCsvPath.split("\\")[-1], originalCsvContent)
