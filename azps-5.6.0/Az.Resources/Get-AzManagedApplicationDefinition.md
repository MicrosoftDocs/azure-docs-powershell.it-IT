---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: f1f71d188a6b25146103fe3fe5d91b8ba53eaaf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985639"
---
# <span data-ttu-id="6dcee-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="6dcee-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="6dcee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dcee-102">SYNOPSIS</span></span>
<span data-ttu-id="6dcee-103">Ottiene le definizioni delle applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="6dcee-103">Gets managed application definitions</span></span>

## <span data-ttu-id="6dcee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dcee-104">SYNTAX</span></span>

### <span data-ttu-id="6dcee-105">GetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6dcee-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcee-106">GetById</span><span class="sxs-lookup"><span data-stu-id="6dcee-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dcee-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6dcee-107">DESCRIPTION</span></span>
<span data-ttu-id="6dcee-108">Il cmdlet **Get-AzManagedApplicationDefinition ottiene** le definizioni delle applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="6dcee-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="6dcee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dcee-109">EXAMPLES</span></span>

### <span data-ttu-id="6dcee-110">Esempio 1: Ottenere tutte le definizioni di applicazioni gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6dcee-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="6dcee-111">Questo comando recupera le definizioni delle applicazioni gestite nel gruppo di risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="6dcee-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="6dcee-112">Esempio 2: Ottenere la definizione di un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="6dcee-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="6dcee-113">Questo comando recupera la definizione di applicazione gestita "myManagedAppDef" nel gruppo di risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="6dcee-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="6dcee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dcee-114">PARAMETERS</span></span>

### <span data-ttu-id="6dcee-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6dcee-115">-ApiVersion</span></span>
<span data-ttu-id="6dcee-116">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="6dcee-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6dcee-117">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="6dcee-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dcee-118">-DefaultProfile</span></span>
<span data-ttu-id="6dcee-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dcee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dcee-120">-Id</span><span class="sxs-lookup"><span data-stu-id="6dcee-120">-Id</span></span>
<span data-ttu-id="6dcee-121">ID di definizione dell'applicazione gestita completa, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="6dcee-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="6dcee-122">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6dcee-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dcee-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6dcee-123">-Name</span></span>
<span data-ttu-id="6dcee-124">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="6dcee-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dcee-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="6dcee-125">-Pre</span></span>
<span data-ttu-id="6dcee-126">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6dcee-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dcee-127">-ResourceGroupName</span></span>
<span data-ttu-id="6dcee-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6dcee-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dcee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dcee-129">CommonParameters</span></span>
<span data-ttu-id="6dcee-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dcee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dcee-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6dcee-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dcee-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6dcee-132">INPUTS</span></span>

### <span data-ttu-id="6dcee-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6dcee-133">System.String</span></span>

## <span data-ttu-id="6dcee-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dcee-134">OUTPUTS</span></span>

### <span data-ttu-id="6dcee-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6dcee-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6dcee-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="6dcee-136">NOTES</span></span>

## <span data-ttu-id="6dcee-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dcee-137">RELATED LINKS</span></span>
