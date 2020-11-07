---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 9d59a974a29743004228efb414a92627782bd8e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687267"
---
# <span data-ttu-id="20a02-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20a02-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="20a02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20a02-102">SYNOPSIS</span></span>
<span data-ttu-id="20a02-103">Rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="20a02-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20a02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20a02-104">SYNTAX</span></span>

### <span data-ttu-id="20a02-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20a02-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20a02-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="20a02-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20a02-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20a02-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20a02-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20a02-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20a02-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20a02-109">DESCRIPTION</span></span>
<span data-ttu-id="20a02-110">Il cmdlet **Remove-AzureRmPolicyDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="20a02-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="20a02-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20a02-111">EXAMPLES</span></span>

### <span data-ttu-id="20a02-112">Esempio 1: rimuovere la definizione dei criteri in base al nome</span><span class="sxs-lookup"><span data-stu-id="20a02-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="20a02-113">Questo comando rimuove la definizione di criterio specificata.</span><span class="sxs-lookup"><span data-stu-id="20a02-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="20a02-114">Esempio 2: rimuovere la definizione dei criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="20a02-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="20a02-115">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="20a02-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="20a02-116">Il comando lo archivia nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="20a02-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="20a02-117">Il secondo comando rimuove la definizione dei criteri identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="20a02-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="20a02-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20a02-118">PARAMETERS</span></span>

### <span data-ttu-id="20a02-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="20a02-119">-ApiVersion</span></span>
<span data-ttu-id="20a02-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="20a02-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="20a02-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="20a02-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="20a02-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a02-122">-DefaultProfile</span></span>
<span data-ttu-id="20a02-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="20a02-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20a02-124">-Force</span><span class="sxs-lookup"><span data-stu-id="20a02-124">-Force</span></span>
<span data-ttu-id="20a02-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="20a02-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20a02-126">-ID</span><span class="sxs-lookup"><span data-stu-id="20a02-126">-Id</span></span>
<span data-ttu-id="20a02-127">Specifica l'ID di risorsa completo per la definizione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a02-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="20a02-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="20a02-128">-InformationAction</span></span>
<span data-ttu-id="20a02-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="20a02-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="20a02-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="20a02-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20a02-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="20a02-131">Continue</span></span>
- <span data-ttu-id="20a02-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="20a02-132">Ignore</span></span>
- <span data-ttu-id="20a02-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="20a02-133">Inquire</span></span>
- <span data-ttu-id="20a02-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20a02-134">SilentlyContinue</span></span>
- <span data-ttu-id="20a02-135">Stop</span><span class="sxs-lookup"><span data-stu-id="20a02-135">Stop</span></span>
- <span data-ttu-id="20a02-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="20a02-136">Suspend</span></span>

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

### <span data-ttu-id="20a02-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20a02-137">-InformationVariable</span></span>
<span data-ttu-id="20a02-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="20a02-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20a02-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="20a02-139">-ManagementGroupName</span></span>
<span data-ttu-id="20a02-140">Nome del gruppo di gestione della definizione di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="20a02-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="20a02-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="20a02-141">-Name</span></span>
<span data-ttu-id="20a02-142">Specifica il nome della definizione di criterio rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a02-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a02-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="20a02-143">-Pre</span></span>
<span data-ttu-id="20a02-144">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="20a02-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="20a02-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20a02-145">-SubscriptionId</span></span>
<span data-ttu-id="20a02-146">ID sottoscrizione della definizione di criterio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="20a02-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="20a02-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="20a02-147">-Confirm</span></span>
<span data-ttu-id="20a02-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a02-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a02-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a02-149">-WhatIf</span></span>
<span data-ttu-id="20a02-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20a02-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a02-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20a02-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a02-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a02-152">CommonParameters</span></span>
<span data-ttu-id="20a02-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a02-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a02-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a02-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a02-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20a02-155">INPUTS</span></span>

## <span data-ttu-id="20a02-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20a02-156">OUTPUTS</span></span>

## <span data-ttu-id="20a02-157">Note</span><span class="sxs-lookup"><span data-stu-id="20a02-157">NOTES</span></span>

## <span data-ttu-id="20a02-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20a02-158">RELATED LINKS</span></span>

[<span data-ttu-id="20a02-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20a02-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="20a02-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20a02-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="20a02-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="20a02-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


