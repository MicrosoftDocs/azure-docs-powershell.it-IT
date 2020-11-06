---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 71f3c6ab80fd0ba44d715cb25b4bf690e44359c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511516"
---
# <span data-ttu-id="26e58-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="26e58-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="26e58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26e58-102">SYNOPSIS</span></span>
<span data-ttu-id="26e58-103">Ottiene le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="26e58-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26e58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26e58-104">SYNTAX</span></span>

### <span data-ttu-id="26e58-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26e58-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="26e58-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e58-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="26e58-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e58-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="26e58-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e58-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="26e58-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26e58-109">DESCRIPTION</span></span>
<span data-ttu-id="26e58-110">Il cmdlet **Get-AzureRmPolicyAssignment** ottiene tutte le assegnazioni dei criteri o le assegnazioni particolari.</span><span class="sxs-lookup"><span data-stu-id="26e58-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="26e58-111">Identificare un'assegnazione di criteri per ottenere il nome e l'ambito o l'ID.</span><span class="sxs-lookup"><span data-stu-id="26e58-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="26e58-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26e58-112">EXAMPLES</span></span>

### <span data-ttu-id="26e58-113">Esempio 1: ottenere tutte le assegnazioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="26e58-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="26e58-114">Questo comando ottiene tutte le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="26e58-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="26e58-115">Esempio 2: ottenere una specifica assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="26e58-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="26e58-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando la Get-AzureRMResourceGroup cmdletand lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="26e58-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="26e58-117">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment07 per l'ambito che identifica la proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="26e58-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="26e58-118">Esempio 3: ottenere tutte le assegnazioni dei criteri assegnate a un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="26e58-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="26e58-119">Il primo comando specifica l'ID del gruppo di gestione a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="26e58-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="26e58-120">Il secondo comando ottiene tutte le assegnazioni dei criteri assegnate al gruppo di gestione con l'ID ' myManagementGroup '.</span><span class="sxs-lookup"><span data-stu-id="26e58-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="26e58-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26e58-121">PARAMETERS</span></span>

### <span data-ttu-id="26e58-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26e58-122">-ApiVersion</span></span>
<span data-ttu-id="26e58-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="26e58-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="26e58-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="26e58-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="26e58-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e58-125">-DefaultProfile</span></span>
<span data-ttu-id="26e58-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="26e58-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26e58-127">-ID</span><span class="sxs-lookup"><span data-stu-id="26e58-127">-Id</span></span>
<span data-ttu-id="26e58-128">Specifica l'ID di risorsa completo per l'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e58-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="26e58-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="26e58-129">-IncludeDescendent</span></span>
<span data-ttu-id="26e58-130">Causa l'elenco delle assegnazioni dei criteri restituite che includono tutte le assegnazioni correlate all'ambito specifico, incluse quelle degli ambiti predecessori e quelle degli ambiti discendenti.</span><span class="sxs-lookup"><span data-stu-id="26e58-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="26e58-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="26e58-131">-InformationAction</span></span>
<span data-ttu-id="26e58-132">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="26e58-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="26e58-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="26e58-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26e58-134">Continuare</span><span class="sxs-lookup"><span data-stu-id="26e58-134">Continue</span></span>
- <span data-ttu-id="26e58-135">Ignora</span><span class="sxs-lookup"><span data-stu-id="26e58-135">Ignore</span></span>
- <span data-ttu-id="26e58-136">Informarsi</span><span class="sxs-lookup"><span data-stu-id="26e58-136">Inquire</span></span>
- <span data-ttu-id="26e58-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="26e58-137">SilentlyContinue</span></span>
- <span data-ttu-id="26e58-138">Stop</span><span class="sxs-lookup"><span data-stu-id="26e58-138">Stop</span></span>
- <span data-ttu-id="26e58-139">Sospensione</span><span class="sxs-lookup"><span data-stu-id="26e58-139">Suspend</span></span>

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

### <span data-ttu-id="26e58-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="26e58-140">-InformationVariable</span></span>
<span data-ttu-id="26e58-141">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="26e58-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="26e58-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="26e58-142">-Name</span></span>
<span data-ttu-id="26e58-143">Specifica il nome dell'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e58-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="26e58-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="26e58-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="26e58-145">Specifica l'ID della definizione di criteri delle assegnazioni dei criteri ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e58-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="26e58-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="26e58-146">-Pre</span></span>
<span data-ttu-id="26e58-147">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="26e58-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26e58-148">-Ambito</span><span class="sxs-lookup"><span data-stu-id="26e58-148">-Scope</span></span>
<span data-ttu-id="26e58-149">Specifica l'ambito in cui viene applicato il criterio per l'assegnazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e58-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="26e58-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e58-150">CommonParameters</span></span>
<span data-ttu-id="26e58-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e58-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e58-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e58-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e58-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26e58-153">INPUTS</span></span>

## <span data-ttu-id="26e58-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26e58-154">OUTPUTS</span></span>

## <span data-ttu-id="26e58-155">Note</span><span class="sxs-lookup"><span data-stu-id="26e58-155">NOTES</span></span>

## <span data-ttu-id="26e58-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26e58-156">RELATED LINKS</span></span>

[<span data-ttu-id="26e58-157">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="26e58-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="26e58-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="26e58-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="26e58-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="26e58-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


