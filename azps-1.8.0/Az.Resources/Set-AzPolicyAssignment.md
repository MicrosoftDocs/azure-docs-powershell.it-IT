---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677274"
---
# <span data-ttu-id="437c4-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="437c4-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="437c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="437c4-102">SYNOPSIS</span></span>
<span data-ttu-id="437c4-103">Modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="437c4-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="437c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="437c4-104">SYNTAX</span></span>

### <span data-ttu-id="437c4-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="437c4-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="437c4-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="437c4-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="437c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="437c4-107">DESCRIPTION</span></span>
<span data-ttu-id="437c4-108">Il cmdlet **set-AzPolicyAssignment** modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="437c4-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="437c4-109">Specificare un'assegnazione in base all'ID o al nome e all'ambito.</span><span class="sxs-lookup"><span data-stu-id="437c4-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="437c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="437c4-110">EXAMPLES</span></span>

### <span data-ttu-id="437c4-111">Esempio 1: aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="437c4-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="437c4-112">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="437c4-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="437c4-113">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="437c4-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="437c4-114">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment usando il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="437c4-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="437c4-115">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="437c4-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="437c4-116">Il comando finale aggiorna il nome visualizzato nell'assegnazione dei criteri nel gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="437c4-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="437c4-117">Esempio 2: aggiungere un'identità gestita all'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="437c4-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="437c4-118">Il primo comando consente di ottenere l'assegnazione di criteri denominata PolicyAssignment dalla sottoscrizione corrente tramite il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="437c4-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="437c4-119">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="437c4-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="437c4-120">Il comando finale assegna un'identità gestita all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="437c4-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="437c4-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="437c4-121">PARAMETERS</span></span>

### <span data-ttu-id="437c4-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="437c4-122">-ApiVersion</span></span>
<span data-ttu-id="437c4-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="437c4-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="437c4-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="437c4-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="437c4-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="437c4-125">-AssignIdentity</span></span>
<span data-ttu-id="437c4-126">Genera e assegna un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="437c4-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="437c4-127">L'identità verrà usata per l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="437c4-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="437c4-128">La posizione è obbligatoria per l'assegnazione di un'identità.</span><span class="sxs-lookup"><span data-stu-id="437c4-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="437c4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="437c4-129">-DefaultProfile</span></span>
<span data-ttu-id="437c4-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="437c4-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="437c4-131">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="437c4-131">-Description</span></span>
<span data-ttu-id="437c4-132">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="437c4-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="437c4-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="437c4-133">-DisplayName</span></span>
<span data-ttu-id="437c4-134">Specifica un nuovo nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="437c4-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="437c4-135">-ID</span><span class="sxs-lookup"><span data-stu-id="437c4-135">-Id</span></span>
<span data-ttu-id="437c4-136">Specifica l'ID di risorsa completo per l'assegnazione di criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="437c4-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="437c4-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="437c4-137">-Location</span></span>
<span data-ttu-id="437c4-138">Posizione dell'identità delle risorse dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="437c4-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="437c4-139">Questo è necessario quando viene usato l'opzione-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="437c4-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="437c4-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="437c4-140">-Metadata</span></span>
<span data-ttu-id="437c4-141">Metadati aggiornati per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="437c4-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="437c4-142">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="437c4-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="437c4-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="437c4-143">-Name</span></span>
<span data-ttu-id="437c4-144">Specifica il nome dell'assegnazione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="437c4-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="437c4-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="437c4-145">-NotScope</span></span>
<span data-ttu-id="437c4-146">L'assegnazione dei criteri non è ambiti.</span><span class="sxs-lookup"><span data-stu-id="437c4-146">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="437c4-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="437c4-147">-Pre</span></span>
<span data-ttu-id="437c4-148">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="437c4-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="437c4-149">-Ambito</span><span class="sxs-lookup"><span data-stu-id="437c4-149">-Scope</span></span>
<span data-ttu-id="437c4-150">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="437c4-150">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="437c4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="437c4-151">CommonParameters</span></span>
<span data-ttu-id="437c4-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="437c4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="437c4-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="437c4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="437c4-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="437c4-154">INPUTS</span></span>

### <span data-ttu-id="437c4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="437c4-155">System.String</span></span>

### <span data-ttu-id="437c4-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="437c4-156">System.String[]</span></span>

## <span data-ttu-id="437c4-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="437c4-157">OUTPUTS</span></span>

### <span data-ttu-id="437c4-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="437c4-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="437c4-159">Note</span><span class="sxs-lookup"><span data-stu-id="437c4-159">NOTES</span></span>

## <span data-ttu-id="437c4-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="437c4-160">RELATED LINKS</span></span>

[<span data-ttu-id="437c4-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="437c4-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="437c4-162">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="437c4-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="437c4-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="437c4-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


