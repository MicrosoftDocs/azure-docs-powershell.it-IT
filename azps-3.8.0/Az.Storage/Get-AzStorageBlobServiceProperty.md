---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 65a48a000e5b3e4377ca2518992ad80242f9e4d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019196"
---
# <span data-ttu-id="a1a90-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a1a90-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="a1a90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1a90-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a90-103">Ottiene le proprietà del servizio per i servizi BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a90-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="a1a90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1a90-104">SYNTAX</span></span>

### <span data-ttu-id="a1a90-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1a90-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1a90-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a1a90-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1a90-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="a1a90-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1a90-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1a90-108">DESCRIPTION</span></span>
<span data-ttu-id="a1a90-109">Il cmdlet **Get-AzStorageBlobServiceProperty** ottiene le proprietà del servizio per i servizi BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a90-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="a1a90-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1a90-110">EXAMPLES</span></span>

### <span data-ttu-id="a1a90-111">Esempio 1: ottenere la proprietà servizi BLOB di archiviazione di Azure di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="a1a90-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days 
------------------ ----------------- --------------------- ----------------------------- -------------------------- 
myresourcegroup    mystorageaccount  2018-03-28            False                                                    
```

<span data-ttu-id="a1a90-112">Questo comando ottiene la proprietà servizi BLOB di un account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a1a90-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="a1a90-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1a90-113">PARAMETERS</span></span>

### <span data-ttu-id="a1a90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a90-114">-DefaultProfile</span></span>
<span data-ttu-id="a1a90-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a90-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a90-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a90-116">-ResourceGroupName</span></span>
<span data-ttu-id="a1a90-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a90-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a90-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1a90-118">-ResourceId</span></span>
<span data-ttu-id="a1a90-119">ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="a1a90-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a90-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1a90-120">-StorageAccount</span></span>
<span data-ttu-id="a1a90-121">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a1a90-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a90-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a1a90-122">-StorageAccountName</span></span>
<span data-ttu-id="a1a90-123">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1a90-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a90-124">CommonParameters</span></span>
<span data-ttu-id="a1a90-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a90-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a90-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a90-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1a90-127">INPUTS</span></span>

### <span data-ttu-id="a1a90-128">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1a90-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a1a90-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a1a90-129">System.String</span></span>

## <span data-ttu-id="a1a90-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1a90-130">OUTPUTS</span></span>

### <span data-ttu-id="a1a90-131">Microsoft. Azure. Commands. Management. storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="a1a90-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="a1a90-132">Note</span><span class="sxs-lookup"><span data-stu-id="a1a90-132">NOTES</span></span>

## <span data-ttu-id="a1a90-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1a90-133">RELATED LINKS</span></span>
