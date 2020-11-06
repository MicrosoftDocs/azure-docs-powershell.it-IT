---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520391"
---
# <span data-ttu-id="2fab2-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fab2-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="2fab2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fab2-102">SYNOPSIS</span></span>
<span data-ttu-id="2fab2-103">Modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="2fab2-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fab2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fab2-104">SYNTAX</span></span>

### <span data-ttu-id="2fab2-105">SetByPolicyAssignmentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fab2-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2fab2-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="2fab2-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2fab2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fab2-107">DESCRIPTION</span></span>
<span data-ttu-id="2fab2-108">Il cmdlet **set-AzureRmPolicyAssignment** modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="2fab2-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="2fab2-109">Specificare un'assegnazione in base all'ID o al nome e all'ambito.</span><span class="sxs-lookup"><span data-stu-id="2fab2-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="2fab2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fab2-110">EXAMPLES</span></span>

### <span data-ttu-id="2fab2-111">Esempio 1: aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="2fab2-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="2fab2-112">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2fab2-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="2fab2-113">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2fab2-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="2fab2-114">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment usando il cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2fab2-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2fab2-115">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2fab2-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="2fab2-116">Il comando finale aggiorna il nome visualizzato nell'assegnazione di criteri identificata dalla proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2fab2-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="2fab2-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fab2-117">PARAMETERS</span></span>

### <span data-ttu-id="2fab2-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2fab2-118">-ApiVersion</span></span>
<span data-ttu-id="2fab2-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="2fab2-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2fab2-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="2fab2-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2fab2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fab2-121">-DefaultProfile</span></span>
<span data-ttu-id="2fab2-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2fab2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fab2-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fab2-123">-Description</span></span>
<span data-ttu-id="2fab2-124">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="2fab2-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fab2-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2fab2-125">-DisplayName</span></span>
<span data-ttu-id="2fab2-126">Specifica un nuovo nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2fab2-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fab2-127">-ID</span><span class="sxs-lookup"><span data-stu-id="2fab2-127">-Id</span></span>
<span data-ttu-id="2fab2-128">Specifica l'ID di risorsa completo per l'assegnazione di criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2fab2-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fab2-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2fab2-129">-InformationAction</span></span>
<span data-ttu-id="2fab2-130">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="2fab2-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2fab2-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fab2-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fab2-132">Continuare</span><span class="sxs-lookup"><span data-stu-id="2fab2-132">Continue</span></span>
- <span data-ttu-id="2fab2-133">Ignora</span><span class="sxs-lookup"><span data-stu-id="2fab2-133">Ignore</span></span>
- <span data-ttu-id="2fab2-134">Informarsi</span><span class="sxs-lookup"><span data-stu-id="2fab2-134">Inquire</span></span>
- <span data-ttu-id="2fab2-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2fab2-135">SilentlyContinue</span></span>
- <span data-ttu-id="2fab2-136">Stop</span><span class="sxs-lookup"><span data-stu-id="2fab2-136">Stop</span></span>
- <span data-ttu-id="2fab2-137">Sospensione</span><span class="sxs-lookup"><span data-stu-id="2fab2-137">Suspend</span></span>

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

### <span data-ttu-id="2fab2-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2fab2-138">-InformationVariable</span></span>
<span data-ttu-id="2fab2-139">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="2fab2-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2fab2-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fab2-140">-Name</span></span>
<span data-ttu-id="2fab2-141">Specifica il nome dell'assegnazione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2fab2-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fab2-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="2fab2-142">-NotScope</span></span>
<span data-ttu-id="2fab2-143">L'assegnazione dei criteri non è ambiti.</span><span class="sxs-lookup"><span data-stu-id="2fab2-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fab2-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="2fab2-144">-Pre</span></span>
<span data-ttu-id="2fab2-145">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="2fab2-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2fab2-146">-Ambito</span><span class="sxs-lookup"><span data-stu-id="2fab2-146">-Scope</span></span>
<span data-ttu-id="2fab2-147">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="2fab2-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fab2-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="2fab2-148">-Sku</span></span>
<span data-ttu-id="2fab2-149">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="2fab2-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fab2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fab2-150">CommonParameters</span></span>
<span data-ttu-id="2fab2-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fab2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fab2-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fab2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fab2-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fab2-153">INPUTS</span></span>

### <span data-ttu-id="2fab2-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2fab2-154">None</span></span>
<span data-ttu-id="2fab2-155">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2fab2-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fab2-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fab2-156">OUTPUTS</span></span>

### <span data-ttu-id="2fab2-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2fab2-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2fab2-158">Note</span><span class="sxs-lookup"><span data-stu-id="2fab2-158">NOTES</span></span>

## <span data-ttu-id="2fab2-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fab2-159">RELATED LINKS</span></span>

[<span data-ttu-id="2fab2-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fab2-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2fab2-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fab2-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2fab2-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fab2-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


