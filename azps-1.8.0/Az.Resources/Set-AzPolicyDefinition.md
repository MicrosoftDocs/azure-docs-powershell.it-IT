---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: f96ea5b7f36806378dff31cc81d211074638342c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677273"
---
# <span data-ttu-id="53b16-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="53b16-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="53b16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53b16-102">SYNOPSIS</span></span>
<span data-ttu-id="53b16-103">Modifica la definizione di un criterio.</span><span class="sxs-lookup"><span data-stu-id="53b16-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="53b16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53b16-104">SYNTAX</span></span>

### <span data-ttu-id="53b16-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53b16-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b16-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b16-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b16-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53b16-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53b16-109">DESCRIPTION</span></span>
<span data-ttu-id="53b16-110">Il cmdlet **set-AzPolicyDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="53b16-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="53b16-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53b16-111">EXAMPLES</span></span>

### <span data-ttu-id="53b16-112">Esempio 1: aggiornare la descrizione di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="53b16-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="53b16-113">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="53b16-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="53b16-114">Il comando Archivia l'oggetto nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="53b16-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="53b16-115">Il secondo comando Aggiorna la descrizione della definizione di criterio identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="53b16-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="53b16-116">Esempio 2: aggiornare la modalità di una definizione di criteri</span><span class="sxs-lookup"><span data-stu-id="53b16-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="53b16-117">Questo comando Aggiorna la definizione dei criteri denominata VMPolicyDefinition usando il cmdlet Set-AzPolicyDefinition per impostare la proprietà Mode su "tutti".</span><span class="sxs-lookup"><span data-stu-id="53b16-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="53b16-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53b16-118">PARAMETERS</span></span>

### <span data-ttu-id="53b16-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53b16-119">-ApiVersion</span></span>
<span data-ttu-id="53b16-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="53b16-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="53b16-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="53b16-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="53b16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b16-122">-DefaultProfile</span></span>
<span data-ttu-id="53b16-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="53b16-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53b16-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="53b16-124">-Description</span></span>
<span data-ttu-id="53b16-125">Specifica una nuova descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="53b16-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="53b16-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="53b16-126">-DisplayName</span></span>
<span data-ttu-id="53b16-127">Specifica un nuovo nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="53b16-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="53b16-128">-ID</span><span class="sxs-lookup"><span data-stu-id="53b16-128">-Id</span></span>
<span data-ttu-id="53b16-129">Specifica l'ID di risorsa completo per la definizione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="53b16-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="53b16-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="53b16-130">-ManagementGroupName</span></span>
<span data-ttu-id="53b16-131">Nome del gruppo di gestione della definizione di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="53b16-131">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="53b16-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="53b16-132">-Metadata</span></span>
<span data-ttu-id="53b16-133">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="53b16-133">The metadata for policy definition.</span></span> <span data-ttu-id="53b16-134">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="53b16-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="53b16-135">-Modalità</span><span class="sxs-lookup"><span data-stu-id="53b16-135">-Mode</span></span>
<span data-ttu-id="53b16-136">Modalità della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="53b16-136">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="53b16-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="53b16-137">-Name</span></span>
<span data-ttu-id="53b16-138">Specifica il nome della definizione di criterio che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="53b16-138">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="53b16-139">Parametro-</span><span class="sxs-lookup"><span data-stu-id="53b16-139">-Parameter</span></span>
<span data-ttu-id="53b16-140">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="53b16-140">The parameters declaration for policy definition.</span></span> <span data-ttu-id="53b16-141">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="53b16-141">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="53b16-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="53b16-142">-Policy</span></span>
<span data-ttu-id="53b16-143">Specifica la nuova regola dei criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="53b16-143">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="53b16-144">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="53b16-144">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="53b16-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="53b16-145">-Pre</span></span>
<span data-ttu-id="53b16-146">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="53b16-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53b16-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53b16-147">-SubscriptionId</span></span>
<span data-ttu-id="53b16-148">ID sottoscrizione della definizione di criterio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="53b16-148">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="53b16-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b16-149">CommonParameters</span></span>
<span data-ttu-id="53b16-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b16-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b16-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b16-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b16-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53b16-152">INPUTS</span></span>

### <span data-ttu-id="53b16-153">System. String</span><span class="sxs-lookup"><span data-stu-id="53b16-153">System.String</span></span>

### <span data-ttu-id="53b16-154">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="53b16-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="53b16-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53b16-155">OUTPUTS</span></span>

### <span data-ttu-id="53b16-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="53b16-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="53b16-157">Note</span><span class="sxs-lookup"><span data-stu-id="53b16-157">NOTES</span></span>

## <span data-ttu-id="53b16-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53b16-158">RELATED LINKS</span></span>

[<span data-ttu-id="53b16-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="53b16-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="53b16-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="53b16-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="53b16-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="53b16-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

