---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509563"
---
# <span data-ttu-id="09661-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09661-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="09661-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09661-102">SYNOPSIS</span></span>
<span data-ttu-id="09661-103">Ottiene un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="09661-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09661-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09661-104">SYNTAX</span></span>

### <span data-ttu-id="09661-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="09661-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="09661-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09661-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="09661-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09661-107">DESCRIPTION</span></span>
<span data-ttu-id="09661-108">Il cmdlet **Get-AzureRmStorageAccount** ottiene un account di archiviazione specificato o tutti gli account di archiviazione in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="09661-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="09661-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09661-109">EXAMPLES</span></span>

### <span data-ttu-id="09661-110">Esempio 1: ottenere un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="09661-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="09661-111">Questo comando ottiene l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="09661-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="09661-112">Esempio 2: ottenere tutti gli account di archiviazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="09661-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="09661-113">Questo comando consente di ottenere tutti gli account di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09661-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="09661-114">Esempio 3: ottenere tutti gli account di archiviazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="09661-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="09661-115">Questo comando consente di ottenere tutti gli account di archiviazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="09661-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="09661-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09661-116">PARAMETERS</span></span>

### <span data-ttu-id="09661-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="09661-117">-Name</span></span>
<span data-ttu-id="09661-118">Specifica il nome dell'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="09661-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09661-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09661-119">-ResourceGroupName</span></span>
<span data-ttu-id="09661-120">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="09661-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09661-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09661-121">CommonParameters</span></span>
<span data-ttu-id="09661-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09661-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09661-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09661-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09661-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09661-124">INPUTS</span></span>

### <span data-ttu-id="09661-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09661-125">None</span></span>
<span data-ttu-id="09661-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="09661-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09661-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09661-127">OUTPUTS</span></span>

## <span data-ttu-id="09661-128">Note</span><span class="sxs-lookup"><span data-stu-id="09661-128">NOTES</span></span>

## <span data-ttu-id="09661-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09661-129">RELATED LINKS</span></span>

[<span data-ttu-id="09661-130">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09661-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="09661-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09661-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="09661-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09661-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
