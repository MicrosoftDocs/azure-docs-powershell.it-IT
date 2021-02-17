---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186118"
---
# <span data-ttu-id="171ce-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="171ce-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="171ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="171ce-102">SYNOPSIS</span></span>
<span data-ttu-id="171ce-103">Ottiene informazioni sugli account di Condivisione dati</span><span class="sxs-lookup"><span data-stu-id="171ce-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="171ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="171ce-104">SYNTAX</span></span>

### <span data-ttu-id="171ce-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="171ce-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="171ce-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="171ce-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="171ce-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="171ce-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="171ce-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="171ce-108">DESCRIPTION</span></span>
<span data-ttu-id="171ce-109">Il cmdlet **Get-AzDataShareAccount** ottiene informazioni sugli account di condivisione dati in una sottoscrizione o un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="171ce-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="171ce-110">Se si specifica il nome di un account, questo cmdlet ottiene informazioni sull'account datshare.</span><span class="sxs-lookup"><span data-stu-id="171ce-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="171ce-111">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti gli account di condivisione dati in una sottoscrizione o un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="171ce-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="171ce-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="171ce-112">EXAMPLES</span></span>

### <span data-ttu-id="171ce-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="171ce-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="171ce-114">Questo comando visualizza informazioni su tutti gli account di condivisione dati nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="171ce-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="171ce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="171ce-115">PARAMETERS</span></span>

### <span data-ttu-id="171ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171ce-116">-DefaultProfile</span></span>
<span data-ttu-id="171ce-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="171ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="171ce-118">-Name</span><span class="sxs-lookup"><span data-stu-id="171ce-118">-Name</span></span>
<span data-ttu-id="171ce-119">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="171ce-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="171ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="171ce-121">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="171ce-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171ce-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="171ce-122">-ResourceId</span></span>
<span data-ttu-id="171ce-123">ID risorsa dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="171ce-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171ce-124">CommonParameters</span></span>
<span data-ttu-id="171ce-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="171ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171ce-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="171ce-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171ce-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="171ce-127">INPUTS</span></span>

### <span data-ttu-id="171ce-128">System.String</span><span class="sxs-lookup"><span data-stu-id="171ce-128">System.String</span></span>

## <span data-ttu-id="171ce-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="171ce-129">OUTPUTS</span></span>

### <span data-ttu-id="171ce-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="171ce-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="171ce-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="171ce-131">NOTES</span></span>

## <span data-ttu-id="171ce-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="171ce-132">RELATED LINKS</span></span>
