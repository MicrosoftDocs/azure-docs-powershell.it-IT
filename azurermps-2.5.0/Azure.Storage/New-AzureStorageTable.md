---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 4fe02c9824945593de4b4160e9db10b1573a335a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866404"
---
# <span data-ttu-id="16acc-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="16acc-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="16acc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16acc-102">SYNOPSIS</span></span>
<span data-ttu-id="16acc-103">Crea una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="16acc-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16acc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16acc-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16acc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16acc-105">DESCRIPTION</span></span>
<span data-ttu-id="16acc-106">Il cmdlet **New-AzureStorageTable** crea una tabella di archiviazione associata all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="16acc-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="16acc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16acc-107">EXAMPLES</span></span>

### <span data-ttu-id="16acc-108">Esempio 1: creare una tabella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="16acc-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="16acc-109">Questo comando crea una tabella di archiviazione con il nome tableabc.</span><span class="sxs-lookup"><span data-stu-id="16acc-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="16acc-110">Esempio 2: creare più tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="16acc-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="16acc-111">Questo comando crea più tabelle.</span><span class="sxs-lookup"><span data-stu-id="16acc-111">This command creates multiple tables.</span></span>
<span data-ttu-id="16acc-112">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="16acc-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="16acc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16acc-113">PARAMETERS</span></span>

### <span data-ttu-id="16acc-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="16acc-114">-Context</span></span>
<span data-ttu-id="16acc-115">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="16acc-115">Specifies the storage context.</span></span>
<span data-ttu-id="16acc-116">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="16acc-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="16acc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16acc-117">-DefaultProfile</span></span>
<span data-ttu-id="16acc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16acc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16acc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="16acc-119">-Name</span></span>
<span data-ttu-id="16acc-120">Specifica un nome per la nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="16acc-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="16acc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16acc-121">CommonParameters</span></span>
<span data-ttu-id="16acc-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16acc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16acc-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16acc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16acc-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16acc-124">INPUTS</span></span>

### <span data-ttu-id="16acc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="16acc-125">System.String</span></span>

### <span data-ttu-id="16acc-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="16acc-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="16acc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16acc-127">OUTPUTS</span></span>

### <span data-ttu-id="16acc-128">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="16acc-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="16acc-129">Note</span><span class="sxs-lookup"><span data-stu-id="16acc-129">NOTES</span></span>

## <span data-ttu-id="16acc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16acc-130">RELATED LINKS</span></span>

[<span data-ttu-id="16acc-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="16acc-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="16acc-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="16acc-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


