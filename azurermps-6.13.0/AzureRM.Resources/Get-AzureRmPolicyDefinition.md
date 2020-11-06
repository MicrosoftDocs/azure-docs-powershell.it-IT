---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 30e113ca85c24b46d4594658f1d91abb6b14bd3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514855"
---
# <span data-ttu-id="6ca1b-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6ca1b-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="6ca1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ca1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca1b-103">Ottiene le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ca1b-104">SYNTAX</span></span>

### <span data-ttu-id="6ca1b-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ca1b-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6ca1b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca1b-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6ca1b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca1b-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6ca1b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca1b-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6ca1b-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca1b-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6ca1b-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca1b-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ca1b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ca1b-111">DESCRIPTION</span></span>
<span data-ttu-id="6ca1b-112">Il cmdlet **Get-AzureRmPolicyDefinition** ottiene una raccolta di definizioni di criteri o una definizione di criteri specifica identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-112">The **Get-AzureRmPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="6ca1b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ca1b-113">EXAMPLES</span></span>

### <span data-ttu-id="6ca1b-114">Esempio 1: ottenere tutte le definizioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="6ca1b-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition
```

<span data-ttu-id="6ca1b-115">Questo comando ottiene tutte le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="6ca1b-116">Esempio 2: ottenere la definizione dei criteri dall'abbonamento corrente per nome</span><span class="sxs-lookup"><span data-stu-id="6ca1b-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="6ca1b-117">Questo comando ottiene la definizione dei criteri denominata VMPolicyDefinition dall'abbonamento predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="6ca1b-118">Esempio 3: ottenere la definizione dei criteri dal gruppo di gestione per nome</span><span class="sxs-lookup"><span data-stu-id="6ca1b-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="6ca1b-119">Questo comando ottiene la definizione dei criteri denominata VMPolicyDefinition dal gruppo di gestione denominato Dept42.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="6ca1b-120">Esempio 4: ottenere tutte le definizioni dei criteri predefinite dall'abbonamento</span><span class="sxs-lookup"><span data-stu-id="6ca1b-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="6ca1b-121">Questo comando consente di ottenere tutte le definizioni dei criteri predefinite dall'abbonamento con ID 3bf44b72-C631-427a-B8C8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="6ca1b-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ca1b-122">PARAMETERS</span></span>

### <span data-ttu-id="6ca1b-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6ca1b-123">-ApiVersion</span></span>
<span data-ttu-id="6ca1b-124">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6ca1b-125">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6ca1b-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="6ca1b-126">-Builtin</span></span>
<span data-ttu-id="6ca1b-127">Limita l'elenco dei risultati per le definizioni di criteri predefinite.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-127">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca1b-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="6ca1b-128">-Custom</span></span>
<span data-ttu-id="6ca1b-129">Limita l'elenco dei risultati solo alle definizioni di criteri personalizzate.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-129">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca1b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca1b-130">-DefaultProfile</span></span>
<span data-ttu-id="6ca1b-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6ca1b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ca1b-132">-ID</span><span class="sxs-lookup"><span data-stu-id="6ca1b-132">-Id</span></span>
<span data-ttu-id="6ca1b-133">Specifica l'ID risorsa completo per la definizione dei criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6ca1b-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ca1b-134">-InformationAction</span></span>
<span data-ttu-id="6ca1b-135">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="6ca1b-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ca1b-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ca1b-137">Continuare</span><span class="sxs-lookup"><span data-stu-id="6ca1b-137">Continue</span></span>
- <span data-ttu-id="6ca1b-138">Ignora</span><span class="sxs-lookup"><span data-stu-id="6ca1b-138">Ignore</span></span>
- <span data-ttu-id="6ca1b-139">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6ca1b-139">Inquire</span></span>
- <span data-ttu-id="6ca1b-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ca1b-140">SilentlyContinue</span></span>
- <span data-ttu-id="6ca1b-141">Stop</span><span class="sxs-lookup"><span data-stu-id="6ca1b-141">Stop</span></span>
- <span data-ttu-id="6ca1b-142">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6ca1b-142">Suspend</span></span>

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

### <span data-ttu-id="6ca1b-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ca1b-143">-InformationVariable</span></span>
<span data-ttu-id="6ca1b-144">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ca1b-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca1b-145">-ManagementGroupName</span></span>
<span data-ttu-id="6ca1b-146">Nome del gruppo di gestione delle definizioni dei criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-146">The name of the management group of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca1b-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ca1b-147">-Name</span></span>
<span data-ttu-id="6ca1b-148">Specifica il nome della definizione del criterio ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca1b-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="6ca1b-149">-Pre</span></span>
<span data-ttu-id="6ca1b-150">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6ca1b-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ca1b-151">-SubscriptionId</span></span>
<span data-ttu-id="6ca1b-152">ID della sottoscrizione delle definizioni dei criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-152">The subscription ID of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca1b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca1b-153">CommonParameters</span></span>
<span data-ttu-id="6ca1b-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca1b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca1b-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca1b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca1b-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ca1b-156">INPUTS</span></span>

## <span data-ttu-id="6ca1b-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ca1b-157">OUTPUTS</span></span>

## <span data-ttu-id="6ca1b-158">Note</span><span class="sxs-lookup"><span data-stu-id="6ca1b-158">NOTES</span></span>

## <span data-ttu-id="6ca1b-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ca1b-159">RELATED LINKS</span></span>

[<span data-ttu-id="6ca1b-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6ca1b-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6ca1b-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6ca1b-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6ca1b-162">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6ca1b-162">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)

