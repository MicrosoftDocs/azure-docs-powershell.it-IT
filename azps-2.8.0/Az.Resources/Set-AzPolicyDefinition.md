---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 4016809ed2592c5d10bc284e4a692381d7965107
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856318"
---
# <span data-ttu-id="567e6-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="567e6-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="567e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="567e6-102">SYNOPSIS</span></span>
<span data-ttu-id="567e6-103">Modifica la definizione di un criterio.</span><span class="sxs-lookup"><span data-stu-id="567e6-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="567e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="567e6-104">SYNTAX</span></span>

### <span data-ttu-id="567e6-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="567e6-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="567e6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="567e6-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="567e6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="567e6-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="567e6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="567e6-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="567e6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="567e6-109">DESCRIPTION</span></span>
<span data-ttu-id="567e6-110">Il cmdlet **set-AzPolicyDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="567e6-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="567e6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="567e6-111">EXAMPLES</span></span>

### <span data-ttu-id="567e6-112">Esempio 1: aggiornare la descrizione di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="567e6-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="567e6-113">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="567e6-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="567e6-114">Il comando Archivia l'oggetto nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="567e6-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="567e6-115">Il secondo comando Aggiorna la descrizione della definizione di criterio identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="567e6-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="567e6-116">Esempio 2: aggiornare la modalità di una definizione di criteri</span><span class="sxs-lookup"><span data-stu-id="567e6-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="567e6-117">Questo comando Aggiorna la definizione dei criteri denominata VMPolicyDefinition usando il cmdlet Set-AzPolicyDefinition per impostare la proprietà Mode su "tutti".</span><span class="sxs-lookup"><span data-stu-id="567e6-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="567e6-118">Esempio 3: aggiornare i metadati di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="567e6-118">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="567e6-119">Questo comando Aggiorna i metadati di una definizione di criteri denominata VMPolicyDefinition per indicare che la relativa categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="567e6-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="567e6-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="567e6-120">PARAMETERS</span></span>

### <span data-ttu-id="567e6-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="567e6-121">-ApiVersion</span></span>
<span data-ttu-id="567e6-122">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="567e6-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="567e6-123">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="567e6-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="567e6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567e6-124">-DefaultProfile</span></span>
<span data-ttu-id="567e6-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="567e6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="567e6-126">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="567e6-126">-Description</span></span>
<span data-ttu-id="567e6-127">Specifica una nuova descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="567e6-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="567e6-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="567e6-128">-DisplayName</span></span>
<span data-ttu-id="567e6-129">Specifica un nuovo nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="567e6-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="567e6-130">-ID</span><span class="sxs-lookup"><span data-stu-id="567e6-130">-Id</span></span>
<span data-ttu-id="567e6-131">Specifica l'ID di risorsa completo per la definizione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="567e6-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="567e6-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="567e6-132">-ManagementGroupName</span></span>
<span data-ttu-id="567e6-133">Nome del gruppo di gestione della definizione di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="567e6-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="567e6-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="567e6-134">-Metadata</span></span>
<span data-ttu-id="567e6-135">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="567e6-135">The metadata for policy definition.</span></span> <span data-ttu-id="567e6-136">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="567e6-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="567e6-137">-Modalità</span><span class="sxs-lookup"><span data-stu-id="567e6-137">-Mode</span></span>
<span data-ttu-id="567e6-138">Modalità della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="567e6-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="567e6-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="567e6-139">-Name</span></span>
<span data-ttu-id="567e6-140">Specifica il nome della definizione di criterio che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="567e6-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="567e6-141">Parametro-</span><span class="sxs-lookup"><span data-stu-id="567e6-141">-Parameter</span></span>
<span data-ttu-id="567e6-142">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="567e6-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="567e6-143">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="567e6-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="567e6-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="567e6-144">-Policy</span></span>
<span data-ttu-id="567e6-145">Specifica la nuova regola dei criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="567e6-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="567e6-146">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="567e6-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="567e6-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="567e6-147">-Pre</span></span>
<span data-ttu-id="567e6-148">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="567e6-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="567e6-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="567e6-149">-SubscriptionId</span></span>
<span data-ttu-id="567e6-150">ID sottoscrizione della definizione di criterio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="567e6-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="567e6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567e6-151">CommonParameters</span></span>
<span data-ttu-id="567e6-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567e6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567e6-153">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="567e6-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567e6-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="567e6-154">INPUTS</span></span>

### <span data-ttu-id="567e6-155">System. String</span><span class="sxs-lookup"><span data-stu-id="567e6-155">System.String</span></span>

### <span data-ttu-id="567e6-156">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="567e6-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="567e6-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="567e6-157">OUTPUTS</span></span>

### <span data-ttu-id="567e6-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="567e6-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="567e6-159">Note</span><span class="sxs-lookup"><span data-stu-id="567e6-159">NOTES</span></span>

## <span data-ttu-id="567e6-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="567e6-160">RELATED LINKS</span></span>

[<span data-ttu-id="567e6-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="567e6-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="567e6-162">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="567e6-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="567e6-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="567e6-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


