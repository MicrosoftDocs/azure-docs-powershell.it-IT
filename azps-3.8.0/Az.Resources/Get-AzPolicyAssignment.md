---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020580"
---
# <span data-ttu-id="4d6db-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4d6db-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="4d6db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d6db-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6db-103">Ottiene le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="4d6db-103">Gets policy assignments.</span></span>

## <span data-ttu-id="4d6db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d6db-104">SYNTAX</span></span>

### <span data-ttu-id="4d6db-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d6db-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d6db-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d6db-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d6db-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d6db-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d6db-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d6db-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d6db-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d6db-109">DESCRIPTION</span></span>
<span data-ttu-id="4d6db-110">Il cmdlet **Get-AzPolicyAssignment** ottiene tutte le assegnazioni dei criteri o le assegnazioni particolari.</span><span class="sxs-lookup"><span data-stu-id="4d6db-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="4d6db-111">Identificare un'assegnazione di criteri per ottenere il nome e l'ambito o l'ID.</span><span class="sxs-lookup"><span data-stu-id="4d6db-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="4d6db-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d6db-112">EXAMPLES</span></span>

### <span data-ttu-id="4d6db-113">Esempio 1: ottenere tutte le assegnazioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="4d6db-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="4d6db-114">Questo comando ottiene tutte le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="4d6db-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="4d6db-115">Esempio 2: ottenere una specifica assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="4d6db-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="4d6db-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4d6db-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4d6db-117">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment07 per l'ambito che identifica la proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4d6db-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="4d6db-118">Esempio 3: ottenere tutte le assegnazioni dei criteri assegnate a un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="4d6db-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="4d6db-119">Il primo comando specifica l'ID del gruppo di gestione a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="4d6db-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="4d6db-120">Il secondo comando ottiene tutte le assegnazioni dei criteri assegnate al gruppo di gestione con l'ID ' myManagementGroup '.</span><span class="sxs-lookup"><span data-stu-id="4d6db-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="4d6db-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d6db-121">PARAMETERS</span></span>

### <span data-ttu-id="4d6db-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4d6db-122">-ApiVersion</span></span>
<span data-ttu-id="4d6db-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="4d6db-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4d6db-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="4d6db-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4d6db-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6db-125">-DefaultProfile</span></span>
<span data-ttu-id="4d6db-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4d6db-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d6db-127">-ID</span><span class="sxs-lookup"><span data-stu-id="4d6db-127">-Id</span></span>
<span data-ttu-id="4d6db-128">Specifica l'ID di risorsa completo per l'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6db-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6db-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="4d6db-129">-IncludeDescendent</span></span>
<span data-ttu-id="4d6db-130">Causa l'elenco delle assegnazioni dei criteri restituite che includono tutte le assegnazioni correlate all'ambito specifico, incluse quelle degli ambiti predecessori e quelle degli ambiti discendenti.</span><span class="sxs-lookup"><span data-stu-id="4d6db-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6db-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d6db-131">-Name</span></span>
<span data-ttu-id="4d6db-132">Specifica il nome dell'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6db-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6db-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4d6db-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="4d6db-134">Specifica l'ID della definizione di criteri delle assegnazioni dei criteri ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6db-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6db-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="4d6db-135">-Pre</span></span>
<span data-ttu-id="4d6db-136">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4d6db-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4d6db-137">-Ambito</span><span class="sxs-lookup"><span data-stu-id="4d6db-137">-Scope</span></span>
<span data-ttu-id="4d6db-138">Specifica l'ambito in cui viene applicato il criterio per l'assegnazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6db-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6db-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6db-139">CommonParameters</span></span>
<span data-ttu-id="4d6db-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d6db-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6db-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d6db-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6db-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d6db-142">INPUTS</span></span>

### <span data-ttu-id="4d6db-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4d6db-143">System.String</span></span>

### <span data-ttu-id="4d6db-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d6db-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d6db-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d6db-145">OUTPUTS</span></span>

### <span data-ttu-id="4d6db-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4d6db-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4d6db-147">Note</span><span class="sxs-lookup"><span data-stu-id="4d6db-147">NOTES</span></span>

## <span data-ttu-id="4d6db-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d6db-148">RELATED LINKS</span></span>

[<span data-ttu-id="4d6db-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4d6db-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="4d6db-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4d6db-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="4d6db-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4d6db-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


