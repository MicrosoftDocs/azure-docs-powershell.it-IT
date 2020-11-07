---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687093"
---
# <span data-ttu-id="f936c-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f936c-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f936c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f936c-102">SYNOPSIS</span></span>
<span data-ttu-id="f936c-103">Crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f936c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f936c-104">SYNTAX</span></span>

### <span data-ttu-id="f936c-105">Assegnazione di criteri senza parametri (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f936c-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f936c-106">Assegnazione di criteri con i parametri tramite l'oggetto Parameter Policy</span><span class="sxs-lookup"><span data-stu-id="f936c-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f936c-107">Assegnazione dei criteri con i parametri tramite la stringa del parametro Policy</span><span class="sxs-lookup"><span data-stu-id="f936c-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f936c-108">Assegnazione di criteri con parametri tramite l'oggetto Parameter Set di criteri</span><span class="sxs-lookup"><span data-stu-id="f936c-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f936c-109">Assegnazione di criteri con i parametri tramite la stringa del parametro set di criteri</span><span class="sxs-lookup"><span data-stu-id="f936c-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f936c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f936c-110">DESCRIPTION</span></span>
<span data-ttu-id="f936c-111">Il cmdlet **New-AzureRmPolicyAssignment** crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="f936c-112">Specificare un criterio e un ambito.</span><span class="sxs-lookup"><span data-stu-id="f936c-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="f936c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f936c-113">EXAMPLES</span></span>

### <span data-ttu-id="f936c-114">Esempio 1: assegnazione dei criteri a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f936c-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="f936c-115">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f936c-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="f936c-116">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f936c-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f936c-117">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f936c-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f936c-118">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="f936c-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="f936c-119">Il comando finale assegna il criterio in $Policy a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f936c-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="f936c-120">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f936c-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="f936c-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f936c-121">PARAMETERS</span></span>

### <span data-ttu-id="f936c-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f936c-122">-ApiVersion</span></span>
<span data-ttu-id="f936c-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="f936c-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f936c-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="f936c-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f936c-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f936c-125">-DisplayName</span></span>
<span data-ttu-id="f936c-126">Specifica un nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-126">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f936c-127">-InformationAction</span></span>
<span data-ttu-id="f936c-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="f936c-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f936c-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f936c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f936c-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="f936c-130">Continue</span></span>
- <span data-ttu-id="f936c-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="f936c-131">Ignore</span></span>
- <span data-ttu-id="f936c-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="f936c-132">Inquire</span></span>
- <span data-ttu-id="f936c-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f936c-133">SilentlyContinue</span></span>
- <span data-ttu-id="f936c-134">Stop</span><span class="sxs-lookup"><span data-stu-id="f936c-134">Stop</span></span>
- <span data-ttu-id="f936c-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="f936c-135">Suspend</span></span>

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

### <span data-ttu-id="f936c-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f936c-136">-InformationVariable</span></span>
<span data-ttu-id="f936c-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="f936c-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f936c-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="f936c-138">-Name</span></span>
<span data-ttu-id="f936c-139">Specifica un nome per l'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="f936c-140">-NotScope</span></span>
<span data-ttu-id="f936c-141">Gli ambiti non per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-141">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f936c-142">-PolicyDefinition</span></span>
<span data-ttu-id="f936c-143">Specifica un criterio, come oggetto **PSObject** che contiene la regola dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="f936c-144">-PolicyParameter</span></span>
<span data-ttu-id="f936c-145">Il percorso del file del parametro policy o la stringa del parametro Policy.</span><span class="sxs-lookup"><span data-stu-id="f936c-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="f936c-146">-PolicyParameterObject</span></span>
<span data-ttu-id="f936c-147">Oggetto Parameter. Policy.</span><span class="sxs-lookup"><span data-stu-id="f936c-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f936c-148">-PolicySetDefinition</span></span>
<span data-ttu-id="f936c-149">Oggetto definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="f936c-150">-Pre</span></span>
<span data-ttu-id="f936c-151">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f936c-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f936c-152">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f936c-152">-Scope</span></span>
<span data-ttu-id="f936c-153">Specifica l'ambito in cui assegnare il criterio.</span><span class="sxs-lookup"><span data-stu-id="f936c-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="f936c-154">Ad esempio, per assegnare un criterio a un gruppo di risorse, specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f936c-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="f936c-155">`/subscriptions/`nome del `/resourcegroups/` gruppo di risorse ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="f936c-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f936c-156">-DefaultProfile</span></span>
<span data-ttu-id="f936c-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f936c-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f936c-158">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f936c-158">-Description</span></span>
<span data-ttu-id="f936c-159">Descrizione dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f936c-159">The description for policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="f936c-160">-Sku</span></span>
<span data-ttu-id="f936c-161">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="f936c-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="f936c-162">Impostazioni predefinite per il codice SKU gratuito: nome = a0, Tier = Free</span><span class="sxs-lookup"><span data-stu-id="f936c-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f936c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f936c-163">CommonParameters</span></span>
<span data-ttu-id="f936c-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f936c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f936c-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f936c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f936c-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f936c-166">INPUTS</span></span>

## <span data-ttu-id="f936c-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f936c-167">OUTPUTS</span></span>

### <span data-ttu-id="f936c-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f936c-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f936c-169">Note</span><span class="sxs-lookup"><span data-stu-id="f936c-169">NOTES</span></span>

## <span data-ttu-id="f936c-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f936c-170">RELATED LINKS</span></span>

[<span data-ttu-id="f936c-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f936c-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="f936c-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f936c-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f936c-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f936c-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f936c-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f936c-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


