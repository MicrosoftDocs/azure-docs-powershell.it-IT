---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186502"
---
# <span data-ttu-id="9305b-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9305b-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="9305b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9305b-102">SYNOPSIS</span></span>
<span data-ttu-id="9305b-103">Ottiene le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9305b-103">Gets policy assignments.</span></span>

## <span data-ttu-id="9305b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9305b-104">SYNTAX</span></span>

### <span data-ttu-id="9305b-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="9305b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9305b-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9305b-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9305b-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="9305b-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9305b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9305b-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9305b-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9305b-109">DESCRIPTION</span></span>
<span data-ttu-id="9305b-110">Il cmdlet **Get-AzPolicyAssignment** ottiene tutte le assegnazioni di criteri o specifiche assegnazioni.</span><span class="sxs-lookup"><span data-stu-id="9305b-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="9305b-111">Identificare un'assegnazione di criteri da ottenere in base al nome e all'ambito o in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="9305b-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="9305b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9305b-112">EXAMPLES</span></span>

### <span data-ttu-id="9305b-113">Esempio 1: Ottenere tutte le assegnazioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="9305b-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="9305b-114">Questo comando recupera tutte le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9305b-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="9305b-115">Esempio 2: Ottenere un'assegnazione di criteri specifica</span><span class="sxs-lookup"><span data-stu-id="9305b-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="9305b-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="9305b-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="9305b-117">Il secondo comando ottiene l'assegnazione dei criteri denominata PolicyAssignment07 per l'ambito identificato dalla proprietà **ResourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9305b-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="9305b-118">Esempio 3: Ottenere tutte le assegnazioni dei criteri assegnate a un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9305b-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="9305b-119">Il primo comando specifica l'ID del gruppo di gestione su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="9305b-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="9305b-120">Il secondo comando ottiene tutte le assegnazioni di criteri assegnate al gruppo di gestione con ID 'myManagementGroup'.</span><span class="sxs-lookup"><span data-stu-id="9305b-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="9305b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9305b-121">PARAMETERS</span></span>

### <span data-ttu-id="9305b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9305b-122">-ApiVersion</span></span>
<span data-ttu-id="9305b-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="9305b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9305b-124">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="9305b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9305b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9305b-125">-DefaultProfile</span></span>
<span data-ttu-id="9305b-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="9305b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9305b-127">-Id</span><span class="sxs-lookup"><span data-stu-id="9305b-127">-Id</span></span>
<span data-ttu-id="9305b-128">Specifica l'ID risorsa completo per l'assegnazione dei criteri che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9305b-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9305b-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="9305b-129">-IncludeDescendent</span></span>
<span data-ttu-id="9305b-130">Fa in modo che l'elenco delle assegnazioni di criteri restituite includa tutte le assegnazioni correlate all'ambito specificato, incluse quelle dagli ambiti predecessori e quelle dagli ambiti più comuni.</span><span class="sxs-lookup"><span data-stu-id="9305b-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="9305b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9305b-131">-Name</span></span>
<span data-ttu-id="9305b-132">Specifica il nome dell'assegnazione di criteri che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9305b-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9305b-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9305b-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="9305b-134">Specifica l'ID della definizione dei criteri delle assegnazioni di criteri che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="9305b-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9305b-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="9305b-135">-Pre</span></span>
<span data-ttu-id="9305b-136">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9305b-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9305b-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="9305b-137">-Scope</span></span>
<span data-ttu-id="9305b-138">Specifica l'ambito in cui vengono applicati i criteri per l'assegnazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9305b-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9305b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9305b-139">CommonParameters</span></span>
<span data-ttu-id="9305b-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9305b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9305b-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9305b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9305b-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="9305b-142">INPUTS</span></span>

### <span data-ttu-id="9305b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9305b-143">System.String</span></span>

### <span data-ttu-id="9305b-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9305b-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9305b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9305b-145">OUTPUTS</span></span>

### <span data-ttu-id="9305b-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="9305b-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9305b-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="9305b-147">NOTES</span></span>

## <span data-ttu-id="9305b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9305b-148">RELATED LINKS</span></span>

[<span data-ttu-id="9305b-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9305b-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="9305b-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9305b-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="9305b-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9305b-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


