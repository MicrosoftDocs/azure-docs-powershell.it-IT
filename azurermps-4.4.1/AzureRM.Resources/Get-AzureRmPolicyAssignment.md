---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512996"
---
# <span data-ttu-id="dbd72-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dbd72-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="dbd72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbd72-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd72-103">Ottiene le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="dbd72-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbd72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbd72-104">SYNTAX</span></span>

### <span data-ttu-id="dbd72-105">Set di parametri elenco tutte le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="dbd72-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="dbd72-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="dbd72-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dbd72-107">Set di parametri nome assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="dbd72-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dbd72-108">Set di parametri ID assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="dbd72-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dbd72-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbd72-109">DESCRIPTION</span></span>
<span data-ttu-id="dbd72-110">Il cmdlet **Get-AzureRmPolicyAssignment** ottiene tutte le assegnazioni dei criteri o le assegnazioni particolari.</span><span class="sxs-lookup"><span data-stu-id="dbd72-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="dbd72-111">Identificare un'assegnazione di criteri per ottenere il nome e l'ambito o l'ID.</span><span class="sxs-lookup"><span data-stu-id="dbd72-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="dbd72-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbd72-112">EXAMPLES</span></span>

### <span data-ttu-id="dbd72-113">Esempio 1: ottenere tutte le assegnazioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="dbd72-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="dbd72-114">Questo comando ottiene tutte le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="dbd72-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="dbd72-115">Esempio 2: ottenere una specifica assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="dbd72-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="dbd72-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dbd72-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="dbd72-117">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dbd72-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="dbd72-118">Il secondo comando consente di ottenere l'assegnazione di criteri denominata PolicyAssignment07 per l'ambito che identifica la proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dbd72-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="dbd72-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbd72-119">PARAMETERS</span></span>

### <span data-ttu-id="dbd72-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dbd72-120">-ApiVersion</span></span>
<span data-ttu-id="dbd72-121">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="dbd72-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dbd72-122">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="dbd72-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dbd72-123">-ID</span><span class="sxs-lookup"><span data-stu-id="dbd72-123">-Id</span></span>
<span data-ttu-id="dbd72-124">Specifica l'ID di risorsa completo per l'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd72-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd72-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dbd72-125">-InformationAction</span></span>
<span data-ttu-id="dbd72-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="dbd72-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dbd72-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbd72-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbd72-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="dbd72-128">Continue</span></span>
- <span data-ttu-id="dbd72-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="dbd72-129">Ignore</span></span>
- <span data-ttu-id="dbd72-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="dbd72-130">Inquire</span></span>
- <span data-ttu-id="dbd72-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dbd72-131">SilentlyContinue</span></span>
- <span data-ttu-id="dbd72-132">Stop</span><span class="sxs-lookup"><span data-stu-id="dbd72-132">Stop</span></span>
- <span data-ttu-id="dbd72-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="dbd72-133">Suspend</span></span>

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

### <span data-ttu-id="dbd72-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dbd72-134">-InformationVariable</span></span>
<span data-ttu-id="dbd72-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="dbd72-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dbd72-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbd72-136">-Name</span></span>
<span data-ttu-id="dbd72-137">Specifica il nome dell'assegnazione di criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd72-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd72-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="dbd72-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="dbd72-139">Specifica l'ID della definizione di criteri delle assegnazioni dei criteri ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd72-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd72-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="dbd72-140">-Pre</span></span>
<span data-ttu-id="dbd72-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="dbd72-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dbd72-142">-Ambito</span><span class="sxs-lookup"><span data-stu-id="dbd72-142">-Scope</span></span>
<span data-ttu-id="dbd72-143">Specifica l'ambito in cui viene applicato il criterio per l'assegnazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd72-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd72-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd72-144">-DefaultProfile</span></span>
<span data-ttu-id="dbd72-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd72-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbd72-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd72-146">CommonParameters</span></span>
<span data-ttu-id="dbd72-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd72-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd72-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd72-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd72-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbd72-149">INPUTS</span></span>

## <span data-ttu-id="dbd72-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbd72-150">OUTPUTS</span></span>

### <span data-ttu-id="dbd72-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="dbd72-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dbd72-152">Note</span><span class="sxs-lookup"><span data-stu-id="dbd72-152">NOTES</span></span>

## <span data-ttu-id="dbd72-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbd72-153">RELATED LINKS</span></span>

[<span data-ttu-id="dbd72-154">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dbd72-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dbd72-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dbd72-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dbd72-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dbd72-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


