---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0fd276b8af8c16fdeb4d412029ac884ae3e5e183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687765"
---
# <span data-ttu-id="d120d-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d120d-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="d120d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d120d-102">SYNOPSIS</span></span>
<span data-ttu-id="d120d-103">Modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d120d-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d120d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d120d-104">SYNTAX</span></span>

### <span data-ttu-id="d120d-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d120d-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d120d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d120d-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d120d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d120d-107">DESCRIPTION</span></span>
<span data-ttu-id="d120d-108">Il cmdlet **set-AzureRmPolicyAssignment** modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d120d-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="d120d-109">Specificare un'assegnazione in base all'ID o al nome e all'ambito.</span><span class="sxs-lookup"><span data-stu-id="d120d-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="d120d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d120d-110">EXAMPLES</span></span>

### <span data-ttu-id="d120d-111">Esempio 1: aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="d120d-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="d120d-112">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d120d-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="d120d-113">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d120d-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d120d-114">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment usando il cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="d120d-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="d120d-115">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="d120d-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="d120d-116">Il comando finale aggiorna il nome visualizzato nell'assegnazione dei criteri nel gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d120d-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="d120d-117">Esempio 2: aggiungere un'identità gestita all'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="d120d-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="d120d-118">Il primo comando consente di ottenere l'assegnazione di criteri denominata PolicyAssignment dalla sottoscrizione corrente tramite il cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="d120d-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="d120d-119">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="d120d-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="d120d-120">Il comando finale assegna un'identità gestita all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d120d-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="d120d-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d120d-121">PARAMETERS</span></span>

### <span data-ttu-id="d120d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d120d-122">-ApiVersion</span></span>
<span data-ttu-id="d120d-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d120d-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d120d-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="d120d-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d120d-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d120d-125">-AssignIdentity</span></span>
<span data-ttu-id="d120d-126">Genera e assegna un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d120d-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="d120d-127">L'identità verrà usata per l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="d120d-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="d120d-128">La posizione è obbligatoria per l'assegnazione di un'identità.</span><span class="sxs-lookup"><span data-stu-id="d120d-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="d120d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d120d-129">-DefaultProfile</span></span>
<span data-ttu-id="d120d-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d120d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d120d-131">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d120d-131">-Description</span></span>
<span data-ttu-id="d120d-132">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="d120d-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="d120d-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d120d-133">-DisplayName</span></span>
<span data-ttu-id="d120d-134">Specifica un nuovo nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d120d-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="d120d-135">-ID</span><span class="sxs-lookup"><span data-stu-id="d120d-135">-Id</span></span>
<span data-ttu-id="d120d-136">Specifica l'ID di risorsa completo per l'assegnazione di criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d120d-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d120d-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d120d-137">-InformationAction</span></span>
<span data-ttu-id="d120d-138">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d120d-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d120d-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d120d-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d120d-140">Continuare</span><span class="sxs-lookup"><span data-stu-id="d120d-140">Continue</span></span>
- <span data-ttu-id="d120d-141">Ignora</span><span class="sxs-lookup"><span data-stu-id="d120d-141">Ignore</span></span>
- <span data-ttu-id="d120d-142">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d120d-142">Inquire</span></span>
- <span data-ttu-id="d120d-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d120d-143">SilentlyContinue</span></span>
- <span data-ttu-id="d120d-144">Stop</span><span class="sxs-lookup"><span data-stu-id="d120d-144">Stop</span></span>
- <span data-ttu-id="d120d-145">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d120d-145">Suspend</span></span>

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

### <span data-ttu-id="d120d-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d120d-146">-InformationVariable</span></span>
<span data-ttu-id="d120d-147">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d120d-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d120d-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d120d-148">-Location</span></span>
<span data-ttu-id="d120d-149">Posizione dell'identità delle risorse dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d120d-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="d120d-150">Questo è necessario quando viene usato l'opzione-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="d120d-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="d120d-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d120d-151">-Metadata</span></span>
<span data-ttu-id="d120d-152">Metadati aggiornati per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d120d-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="d120d-153">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="d120d-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="d120d-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="d120d-154">-Name</span></span>
<span data-ttu-id="d120d-155">Specifica il nome dell'assegnazione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d120d-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d120d-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="d120d-156">-NotScope</span></span>
<span data-ttu-id="d120d-157">L'assegnazione dei criteri non è ambiti.</span><span class="sxs-lookup"><span data-stu-id="d120d-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="d120d-158">-Pre</span><span class="sxs-lookup"><span data-stu-id="d120d-158">-Pre</span></span>
<span data-ttu-id="d120d-159">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d120d-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d120d-160">-Ambito</span><span class="sxs-lookup"><span data-stu-id="d120d-160">-Scope</span></span>
<span data-ttu-id="d120d-161">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="d120d-161">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d120d-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="d120d-162">-Sku</span></span>
<span data-ttu-id="d120d-163">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="d120d-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="d120d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d120d-164">CommonParameters</span></span>
<span data-ttu-id="d120d-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d120d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d120d-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d120d-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d120d-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d120d-167">INPUTS</span></span>

## <span data-ttu-id="d120d-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d120d-168">OUTPUTS</span></span>

## <span data-ttu-id="d120d-169">Note</span><span class="sxs-lookup"><span data-stu-id="d120d-169">NOTES</span></span>

## <span data-ttu-id="d120d-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d120d-170">RELATED LINKS</span></span>

[<span data-ttu-id="d120d-171">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d120d-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="d120d-172">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d120d-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="d120d-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d120d-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


