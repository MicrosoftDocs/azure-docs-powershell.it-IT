---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 14f42ae951fe25f7594eb6e314ac65bb678e29c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509479"
---
# <span data-ttu-id="4d15b-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4d15b-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="4d15b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d15b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d15b-103">Crea una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4d15b-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d15b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d15b-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d15b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d15b-105">DESCRIPTION</span></span>
<span data-ttu-id="4d15b-106">Il cmdlet **New-AzureStorageTable** crea una tabella di archiviazione associata all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="4d15b-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="4d15b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d15b-107">EXAMPLES</span></span>

### <span data-ttu-id="4d15b-108">Esempio 1: creare una tabella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4d15b-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="4d15b-109">Questo comando crea una tabella di archiviazione con il nome tableabc.</span><span class="sxs-lookup"><span data-stu-id="4d15b-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="4d15b-110">Esempio 2: creare più tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4d15b-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="4d15b-111">Questo comando crea più tabelle.</span><span class="sxs-lookup"><span data-stu-id="4d15b-111">This command creates multiple tables.</span></span>
<span data-ttu-id="4d15b-112">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d15b-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="4d15b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d15b-113">PARAMETERS</span></span>

### <span data-ttu-id="4d15b-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4d15b-114">-Context</span></span>
<span data-ttu-id="4d15b-115">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4d15b-115">Specifies the storage context.</span></span>
<span data-ttu-id="4d15b-116">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4d15b-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d15b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d15b-117">-DefaultProfile</span></span>
<span data-ttu-id="4d15b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d15b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d15b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d15b-119">-Name</span></span>
<span data-ttu-id="4d15b-120">Specifica un nome per la nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="4d15b-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d15b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d15b-121">CommonParameters</span></span>
<span data-ttu-id="4d15b-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d15b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d15b-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d15b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d15b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d15b-124">INPUTS</span></span>

### <span data-ttu-id="4d15b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4d15b-125">System.String</span></span>

### <span data-ttu-id="4d15b-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4d15b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4d15b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d15b-127">OUTPUTS</span></span>

### <span data-ttu-id="4d15b-128">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4d15b-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="4d15b-129">Note</span><span class="sxs-lookup"><span data-stu-id="4d15b-129">NOTES</span></span>

## <span data-ttu-id="4d15b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d15b-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d15b-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4d15b-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="4d15b-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4d15b-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


