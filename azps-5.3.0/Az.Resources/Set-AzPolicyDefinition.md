---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474148"
---
# <span data-ttu-id="64d8c-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64d8c-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="64d8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="64d8c-103">Modifica la definizione di un criterio.</span><span class="sxs-lookup"><span data-stu-id="64d8c-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="64d8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64d8c-104">SYNTAX</span></span>

### <span data-ttu-id="64d8c-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64d8c-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64d8c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d8c-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64d8c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d8c-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64d8c-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d8c-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64d8c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d8c-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64d8c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64d8c-110">DESCRIPTION</span></span>
<span data-ttu-id="64d8c-111">Il cmdlet **set-AzPolicyDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="64d8c-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="64d8c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64d8c-112">EXAMPLES</span></span>

### <span data-ttu-id="64d8c-113">Esempio 1: aggiornare la descrizione di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="64d8c-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="64d8c-114">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="64d8c-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="64d8c-115">Il comando Archivia l'oggetto nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="64d8c-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="64d8c-116">Il secondo comando Aggiorna la descrizione della definizione di criterio identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="64d8c-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="64d8c-117">Esempio 2: aggiornare la modalità di una definizione di criteri</span><span class="sxs-lookup"><span data-stu-id="64d8c-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="64d8c-118">Questo comando Aggiorna la definizione dei criteri denominata VMPolicyDefinition usando il cmdlet Set-AzPolicyDefinition per impostare la proprietà Mode su "tutti".</span><span class="sxs-lookup"><span data-stu-id="64d8c-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="64d8c-119">Esempio 3: aggiornare i metadati di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="64d8c-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="64d8c-120">Questo comando Aggiorna i metadati di una definizione di criteri denominata VMPolicyDefinition per indicare che la relativa categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="64d8c-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="64d8c-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64d8c-121">PARAMETERS</span></span>

### <span data-ttu-id="64d8c-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="64d8c-122">-ApiVersion</span></span>
<span data-ttu-id="64d8c-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="64d8c-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="64d8c-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="64d8c-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="64d8c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d8c-125">-DefaultProfile</span></span>
<span data-ttu-id="64d8c-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="64d8c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64d8c-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="64d8c-127">-Description</span></span>
<span data-ttu-id="64d8c-128">Specifica una nuova descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="64d8c-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="64d8c-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64d8c-129">-DisplayName</span></span>
<span data-ttu-id="64d8c-130">Specifica un nuovo nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="64d8c-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="64d8c-131">-ID</span><span class="sxs-lookup"><span data-stu-id="64d8c-131">-Id</span></span>
<span data-ttu-id="64d8c-132">Specifica l'ID di risorsa completo per la definizione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="64d8c-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="64d8c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64d8c-133">-InputObject</span></span>
<span data-ttu-id="64d8c-134">Oggetto di definizione dei criteri da aggiornare che è stato restituito da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64d8c-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64d8c-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="64d8c-135">-ManagementGroupName</span></span>
<span data-ttu-id="64d8c-136">Nome del gruppo di gestione della definizione di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="64d8c-136">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d8c-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="64d8c-137">-Metadata</span></span>
<span data-ttu-id="64d8c-138">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="64d8c-138">The metadata for policy definition.</span></span> <span data-ttu-id="64d8c-139">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="64d8c-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="64d8c-140">-Modalità</span><span class="sxs-lookup"><span data-stu-id="64d8c-140">-Mode</span></span>
<span data-ttu-id="64d8c-141">Modalità della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="64d8c-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="64d8c-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="64d8c-142">-Name</span></span>
<span data-ttu-id="64d8c-143">Specifica il nome della definizione di criterio che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="64d8c-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d8c-144">Parametro-</span><span class="sxs-lookup"><span data-stu-id="64d8c-144">-Parameter</span></span>
<span data-ttu-id="64d8c-145">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="64d8c-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="64d8c-146">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="64d8c-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="64d8c-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="64d8c-147">-Policy</span></span>
<span data-ttu-id="64d8c-148">Specifica la nuova regola dei criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="64d8c-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="64d8c-149">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="64d8c-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="64d8c-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="64d8c-150">-Pre</span></span>
<span data-ttu-id="64d8c-151">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="64d8c-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="64d8c-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64d8c-152">-SubscriptionId</span></span>
<span data-ttu-id="64d8c-153">ID sottoscrizione della definizione di criterio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="64d8c-153">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d8c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d8c-154">CommonParameters</span></span>
<span data-ttu-id="64d8c-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d8c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d8c-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64d8c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d8c-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64d8c-157">INPUTS</span></span>

### <span data-ttu-id="64d8c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="64d8c-158">System.String</span></span>

### <span data-ttu-id="64d8c-159">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="64d8c-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="64d8c-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64d8c-160">OUTPUTS</span></span>

### <span data-ttu-id="64d8c-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="64d8c-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="64d8c-162">Note</span><span class="sxs-lookup"><span data-stu-id="64d8c-162">NOTES</span></span>

## <span data-ttu-id="64d8c-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64d8c-163">RELATED LINKS</span></span>

[<span data-ttu-id="64d8c-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64d8c-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="64d8c-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64d8c-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="64d8c-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64d8c-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


