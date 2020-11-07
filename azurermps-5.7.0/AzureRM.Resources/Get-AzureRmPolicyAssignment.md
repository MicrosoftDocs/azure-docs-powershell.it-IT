---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687014"
---
# <span data-ttu-id="3c04e-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3c04e-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="3c04e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c04e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c04e-103">Ottiene le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="3c04e-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c04e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c04e-104">SYNTAX</span></span>

### <span data-ttu-id="3c04e-105">GetAllPolicyAssignments (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c04e-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3c04e-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="3c04e-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3c04e-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="3c04e-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c04e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c04e-108">DESCRIPTION</span></span>
<span data-ttu-id="3c04e-109">Il cmdlet **Get-AzureRmPolicyAssignment** ottiene tutte le assegnazioni dei criteri o le assegnazioni particolari.</span><span class="sxs-lookup"><span data-stu-id="3c04e-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="3c04e-110">Identificare un'assegnazione di criteri per ottenere il nome e l'ambito o l'ID.</span><span class="sxs-lookup"><span data-stu-id="3c04e-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="3c04e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c04e-111">EXAMPLES</span></span>

### <span data-ttu-id="3c04e-112">Esempio 1: ottenere tutte le assegnazioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="3c04e-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="3c04e-113">Questo comando ottiene tutte le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="3c04e-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="3c04e-114">Esempio 2: ottenere una specifica assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="3c04e-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="3c04e-115">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c04e-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="3c04e-116">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c04e-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="3c04e-117">Il secondo comando consente di ottenere l'assegnazione di criteri denominata PolicyAssignment07 per l'ambito che identifica la proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c04e-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="3c04e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c04e-118">PARAMETERS</span></span>

### <span data-ttu-id="3c04e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3c04e-119">-ApiVersion</span></span>
<span data-ttu-id="3c04e-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="3c04e-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3c04e-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="3c04e-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c04e-122">-DefaultProfile</span></span>
<span data-ttu-id="3c04e-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3c04e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="3c04e-124">-Id</span></span>
<span data-ttu-id="3c04e-125">Specifica l'ID di risorsa completo per l'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c04e-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3c04e-126">-InformationAction</span></span>
<span data-ttu-id="3c04e-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="3c04e-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c04e-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c04e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c04e-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="3c04e-129">Continue</span></span>
- <span data-ttu-id="3c04e-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="3c04e-130">Ignore</span></span>
- <span data-ttu-id="3c04e-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="3c04e-131">Inquire</span></span>
- <span data-ttu-id="3c04e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c04e-132">SilentlyContinue</span></span>
- <span data-ttu-id="3c04e-133">Stop</span><span class="sxs-lookup"><span data-stu-id="3c04e-133">Stop</span></span>
- <span data-ttu-id="3c04e-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="3c04e-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c04e-135">-InformationVariable</span></span>
<span data-ttu-id="3c04e-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="3c04e-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c04e-137">-Name</span></span>
<span data-ttu-id="3c04e-138">Specifica il nome dell'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c04e-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3c04e-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="3c04e-140">Specifica l'ID della definizione di criteri delle assegnazioni dei criteri ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c04e-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="3c04e-141">-Pre</span></span>
<span data-ttu-id="3c04e-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3c04e-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="3c04e-143">-Scope</span></span>
<span data-ttu-id="3c04e-144">Specifica l'ambito in cui viene applicato il criterio per l'assegnazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c04e-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c04e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c04e-145">CommonParameters</span></span>
<span data-ttu-id="3c04e-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c04e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c04e-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c04e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c04e-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c04e-148">INPUTS</span></span>

### <span data-ttu-id="3c04e-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3c04e-149">None</span></span>
<span data-ttu-id="3c04e-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3c04e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c04e-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c04e-151">OUTPUTS</span></span>

### <span data-ttu-id="3c04e-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3c04e-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3c04e-153">Note</span><span class="sxs-lookup"><span data-stu-id="3c04e-153">NOTES</span></span>

## <span data-ttu-id="3c04e-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c04e-154">RELATED LINKS</span></span>

[<span data-ttu-id="3c04e-155">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3c04e-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="3c04e-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3c04e-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="3c04e-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3c04e-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


