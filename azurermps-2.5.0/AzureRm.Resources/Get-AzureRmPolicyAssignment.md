---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866446"
---
# <span data-ttu-id="da7b4-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="da7b4-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="da7b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da7b4-102">SYNOPSIS</span></span>
<span data-ttu-id="da7b4-103">Ottiene le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="da7b4-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da7b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da7b4-104">SYNTAX</span></span>

### <span data-ttu-id="da7b4-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da7b4-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="da7b4-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="da7b4-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="da7b4-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="da7b4-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="da7b4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da7b4-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="da7b4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da7b4-109">DESCRIPTION</span></span>
<span data-ttu-id="da7b4-110">Il cmdlet **Get-AzureRmPolicyAssignment** ottiene tutte le assegnazioni dei criteri o le assegnazioni particolari.</span><span class="sxs-lookup"><span data-stu-id="da7b4-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="da7b4-111">Identificare un'assegnazione di criteri per ottenere il nome e l'ambito o l'ID.</span><span class="sxs-lookup"><span data-stu-id="da7b4-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="da7b4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da7b4-112">EXAMPLES</span></span>

### <span data-ttu-id="da7b4-113">Esempio 1: ottenere tutte le assegnazioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="da7b4-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="da7b4-114">Questo comando ottiene tutte le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="da7b4-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="da7b4-115">Esempio 2: ottenere una specifica assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="da7b4-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="da7b4-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando la Get-AzureRMResourceGroup cmdletand lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da7b4-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="da7b4-117">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment07 per l'ambito che identifica la proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da7b4-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="da7b4-118">Esempio 3: ottenere tutte le assegnazioni dei criteri assegnate a un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="da7b4-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="da7b4-119">Il primo comando specifica l'ID del gruppo di gestione a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="da7b4-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="da7b4-120">Il secondo comando ottiene tutte le assegnazioni dei criteri assegnate al gruppo di gestione con l'ID ' myManagementGroup '.</span><span class="sxs-lookup"><span data-stu-id="da7b4-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="da7b4-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da7b4-121">PARAMETERS</span></span>

### <span data-ttu-id="da7b4-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da7b4-122">-ApiVersion</span></span>
<span data-ttu-id="da7b4-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="da7b4-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="da7b4-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="da7b4-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="da7b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7b4-125">-DefaultProfile</span></span>
<span data-ttu-id="da7b4-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="da7b4-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da7b4-127">-ID</span><span class="sxs-lookup"><span data-stu-id="da7b4-127">-Id</span></span>
<span data-ttu-id="da7b4-128">Specifica l'ID di risorsa completo per l'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7b4-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da7b4-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="da7b4-129">-IncludeDescendent</span></span>
<span data-ttu-id="da7b4-130">Causa l'elenco delle assegnazioni dei criteri restituite che includono tutte le assegnazioni correlate all'ambito specifico, incluse quelle degli ambiti predecessori e quelle degli ambiti discendenti.</span><span class="sxs-lookup"><span data-stu-id="da7b4-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="da7b4-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="da7b4-131">-InformationAction</span></span>
<span data-ttu-id="da7b4-132">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="da7b4-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="da7b4-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="da7b4-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da7b4-134">Continuare</span><span class="sxs-lookup"><span data-stu-id="da7b4-134">Continue</span></span>
- <span data-ttu-id="da7b4-135">Ignora</span><span class="sxs-lookup"><span data-stu-id="da7b4-135">Ignore</span></span>
- <span data-ttu-id="da7b4-136">Informarsi</span><span class="sxs-lookup"><span data-stu-id="da7b4-136">Inquire</span></span>
- <span data-ttu-id="da7b4-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="da7b4-137">SilentlyContinue</span></span>
- <span data-ttu-id="da7b4-138">Stop</span><span class="sxs-lookup"><span data-stu-id="da7b4-138">Stop</span></span>
- <span data-ttu-id="da7b4-139">Sospensione</span><span class="sxs-lookup"><span data-stu-id="da7b4-139">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7b4-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="da7b4-140">-InformationVariable</span></span>
<span data-ttu-id="da7b4-141">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="da7b4-141">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7b4-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="da7b4-142">-Name</span></span>
<span data-ttu-id="da7b4-143">Specifica il nome dell'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7b4-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da7b4-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="da7b4-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="da7b4-145">Specifica l'ID della definizione di criteri delle assegnazioni dei criteri ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7b4-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da7b4-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="da7b4-146">-Pre</span></span>
<span data-ttu-id="da7b4-147">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="da7b4-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="da7b4-148">-Ambito</span><span class="sxs-lookup"><span data-stu-id="da7b4-148">-Scope</span></span>
<span data-ttu-id="da7b4-149">Specifica l'ambito in cui viene applicato il criterio per l'assegnazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7b4-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da7b4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7b4-150">CommonParameters</span></span>
<span data-ttu-id="da7b4-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7b4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7b4-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7b4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7b4-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da7b4-153">INPUTS</span></span>

## <span data-ttu-id="da7b4-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da7b4-154">OUTPUTS</span></span>

## <span data-ttu-id="da7b4-155">Note</span><span class="sxs-lookup"><span data-stu-id="da7b4-155">NOTES</span></span>

## <span data-ttu-id="da7b4-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da7b4-156">RELATED LINKS</span></span>

[<span data-ttu-id="da7b4-157">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="da7b4-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="da7b4-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="da7b4-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="da7b4-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="da7b4-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


