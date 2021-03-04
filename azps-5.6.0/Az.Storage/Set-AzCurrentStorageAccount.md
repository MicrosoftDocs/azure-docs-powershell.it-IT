---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: aeda6548526c4ad12746ce90f1a030f85a0a8d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950782"
---
# <span data-ttu-id="a7986-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7986-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="a7986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7986-102">SYNOPSIS</span></span>
<span data-ttu-id="a7986-103">Modifica l'account di archiviazione corrente della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a7986-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="a7986-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7986-104">SYNTAX</span></span>

### <span data-ttu-id="a7986-105">UsingResourceGroupAndNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a7986-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7986-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7986-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7986-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7986-107">DESCRIPTION</span></span>
<span data-ttu-id="a7986-108">Il cmdlet **Set-AzCurrentStorageAccount** modifica l'account di archiviazione di Azure corrente della sottoscrizione di Azure specificata in Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7986-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="a7986-109">L'account di archiviazione corrente viene usato come predefinito quando si accede ad Archiviazione senza specificare un nome di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7986-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="a7986-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7986-110">EXAMPLES</span></span>

### <span data-ttu-id="a7986-111">Esempio 1: Impostare l'account di archiviazione corrente</span><span class="sxs-lookup"><span data-stu-id="a7986-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="a7986-112">Questo comando imposta l'account di archiviazione predefinito per la sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a7986-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="a7986-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7986-113">PARAMETERS</span></span>

### <span data-ttu-id="a7986-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a7986-114">-Context</span></span>
<span data-ttu-id="a7986-115">Specifica un oggetto **AzureStorageContext** per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="a7986-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="a7986-116">Per ottenere un oggetto contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7986-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7986-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7986-117">-DefaultProfile</span></span>
<span data-ttu-id="a7986-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7986-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7986-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a7986-119">-Name</span></span>
<span data-ttu-id="a7986-120">Specifica il nome dell'account di archiviazione modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7986-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7986-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7986-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7986-122">Specifica il gruppo di risorse che contiene l'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="a7986-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7986-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7986-123">CommonParameters</span></span>
<span data-ttu-id="a7986-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7986-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7986-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7986-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7986-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7986-126">INPUTS</span></span>

### <span data-ttu-id="a7986-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7986-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="a7986-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a7986-128">System.String</span></span>

## <span data-ttu-id="a7986-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7986-129">OUTPUTS</span></span>

### <span data-ttu-id="a7986-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a7986-130">System.String</span></span>

## <span data-ttu-id="a7986-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7986-131">NOTES</span></span>

## <span data-ttu-id="a7986-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7986-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7986-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7986-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


