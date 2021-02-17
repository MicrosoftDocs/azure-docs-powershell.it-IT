---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192718"
---
# <span data-ttu-id="26026-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="26026-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="26026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26026-102">SYNOPSIS</span></span>
<span data-ttu-id="26026-103">Modifica una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="26026-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="26026-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26026-104">SYNTAX</span></span>

### <span data-ttu-id="26026-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="26026-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26026-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26026-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26026-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26026-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26026-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26026-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26026-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26026-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26026-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26026-110">DESCRIPTION</span></span>
<span data-ttu-id="26026-111">Il cmdlet **Set-AzPolicyDefinition** modifica una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="26026-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="26026-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26026-112">EXAMPLES</span></span>

### <span data-ttu-id="26026-113">Esempio 1: Aggiornare la descrizione di una definizione di criteri</span><span class="sxs-lookup"><span data-stu-id="26026-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="26026-114">Il primo comando ottiene una definizione di criterio denominata VMPolicyDefinition usando Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26026-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="26026-115">Il comando archivia l'oggetto nella $PolicyDefinition variabile.</span><span class="sxs-lookup"><span data-stu-id="26026-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="26026-116">Il secondo comando aggiorna la descrizione della definizione dei criteri identificata dalla **proprietà ResourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="26026-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="26026-117">Esempio 2: Aggiornare la modalità di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="26026-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="26026-118">Questo comando aggiorna la definizione del criterio denominata VMPolicyDefinition usando il cmdlet Set-AzPolicyDefinition per impostare la proprietà mode su "All".</span><span class="sxs-lookup"><span data-stu-id="26026-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="26026-119">Esempio 3: Aggiornare i metadati di una definizione di criteri</span><span class="sxs-lookup"><span data-stu-id="26026-119">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="26026-120">Questo comando aggiorna i metadati di una definizione di criterio denominata VMPolicyDefinition per indicare che la categoria è "Macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="26026-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="26026-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26026-121">PARAMETERS</span></span>

### <span data-ttu-id="26026-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26026-122">-ApiVersion</span></span>
<span data-ttu-id="26026-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="26026-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="26026-124">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="26026-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="26026-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26026-125">-DefaultProfile</span></span>
<span data-ttu-id="26026-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="26026-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26026-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="26026-127">-Description</span></span>
<span data-ttu-id="26026-128">Specifica una nuova descrizione per la definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="26026-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="26026-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="26026-129">-DisplayName</span></span>
<span data-ttu-id="26026-130">Specifica un nuovo nome visualizzato per la definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="26026-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="26026-131">-Id</span><span class="sxs-lookup"><span data-stu-id="26026-131">-Id</span></span>
<span data-ttu-id="26026-132">Specifica l'ID risorsa completo per la definizione del criterio modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26026-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="26026-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26026-133">-InputObject</span></span>
<span data-ttu-id="26026-134">Oggetto della definizione dei criteri da aggiornare che è stato generato da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26026-134">The policy definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="26026-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="26026-135">-ManagementGroupName</span></span>
<span data-ttu-id="26026-136">Nome del gruppo di gestione della definizione dei criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="26026-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="26026-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="26026-137">-Metadata</span></span>
<span data-ttu-id="26026-138">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="26026-138">The metadata for policy definition.</span></span> <span data-ttu-id="26026-139">Può trattarsi del percorso di un nome file contenente i metadati o dei metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="26026-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="26026-140">-Modalità</span><span class="sxs-lookup"><span data-stu-id="26026-140">-Mode</span></span>
<span data-ttu-id="26026-141">Modalità della definizione del nuovo criterio.</span><span class="sxs-lookup"><span data-stu-id="26026-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="26026-142">-Name</span><span class="sxs-lookup"><span data-stu-id="26026-142">-Name</span></span>
<span data-ttu-id="26026-143">Specifica il nome della definizione del criterio modificata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26026-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="26026-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="26026-144">-Parameter</span></span>
<span data-ttu-id="26026-145">Dichiarazione dei parametri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="26026-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="26026-146">Può trattarsi del percorso di un nome file o di un URI contenente la dichiarazione dei parametri oppure della dichiarazione dei parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="26026-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="26026-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="26026-147">-Policy</span></span>
<span data-ttu-id="26026-148">Specifica una nuova regola per i criteri per la definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="26026-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="26026-149">È possibile specificare il percorso di un file JSON o una stringa che contiene i criteri in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="26026-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="26026-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="26026-150">-Pre</span></span>
<span data-ttu-id="26026-151">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="26026-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26026-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26026-152">-SubscriptionId</span></span>
<span data-ttu-id="26026-153">ID sottoscrizione della definizione dei criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="26026-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="26026-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26026-154">CommonParameters</span></span>
<span data-ttu-id="26026-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26026-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26026-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26026-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26026-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="26026-157">INPUTS</span></span>

### <span data-ttu-id="26026-158">System.String</span><span class="sxs-lookup"><span data-stu-id="26026-158">System.String</span></span>

### <span data-ttu-id="26026-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26026-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="26026-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26026-160">OUTPUTS</span></span>

### <span data-ttu-id="26026-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="26026-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="26026-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="26026-162">NOTES</span></span>

## <span data-ttu-id="26026-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26026-163">RELATED LINKS</span></span>

[<span data-ttu-id="26026-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="26026-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="26026-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="26026-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="26026-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="26026-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


