---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862398"
---
# <span data-ttu-id="dc5f5-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dc5f5-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="dc5f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5f5-103">Rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-103">Removes a policy definition.</span></span>

## <span data-ttu-id="dc5f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc5f5-104">SYNTAX</span></span>

### <span data-ttu-id="dc5f5-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc5f5-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc5f5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc5f5-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc5f5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc5f5-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc5f5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc5f5-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc5f5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc5f5-109">DESCRIPTION</span></span>
<span data-ttu-id="dc5f5-110">Il cmdlet **Remove-AzPolicyDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="dc5f5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc5f5-111">EXAMPLES</span></span>

### <span data-ttu-id="dc5f5-112">Esempio 1: rimuovere la definizione dei criteri in base al nome</span><span class="sxs-lookup"><span data-stu-id="dc5f5-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="dc5f5-113">Questo comando rimuove la definizione di criterio specificata.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="dc5f5-114">Esempio 2: rimuovere la definizione dei criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="dc5f5-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="dc5f5-115">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="dc5f5-116">Il comando lo archivia nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="dc5f5-117">Il secondo comando rimuove la definizione dei criteri identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="dc5f5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc5f5-118">PARAMETERS</span></span>

### <span data-ttu-id="dc5f5-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dc5f5-119">-ApiVersion</span></span>
<span data-ttu-id="dc5f5-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dc5f5-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dc5f5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5f5-122">-DefaultProfile</span></span>
<span data-ttu-id="dc5f5-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dc5f5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5f5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dc5f5-124">-Force</span></span>
<span data-ttu-id="dc5f5-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc5f5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="dc5f5-126">-Id</span></span>
<span data-ttu-id="dc5f5-127">Specifica l'ID di risorsa completo per la definizione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dc5f5-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dc5f5-128">-InformationAction</span></span>
<span data-ttu-id="dc5f5-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="dc5f5-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc5f5-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dc5f5-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="dc5f5-131">Continue</span></span>
- <span data-ttu-id="dc5f5-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="dc5f5-132">Ignore</span></span>
- <span data-ttu-id="dc5f5-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="dc5f5-133">Inquire</span></span>
- <span data-ttu-id="dc5f5-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dc5f5-134">SilentlyContinue</span></span>
- <span data-ttu-id="dc5f5-135">Stop</span><span class="sxs-lookup"><span data-stu-id="dc5f5-135">Stop</span></span>
- <span data-ttu-id="dc5f5-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="dc5f5-136">Suspend</span></span>

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

### <span data-ttu-id="dc5f5-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dc5f5-137">-InformationVariable</span></span>
<span data-ttu-id="dc5f5-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dc5f5-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5f5-139">-ManagementGroupName</span></span>
<span data-ttu-id="dc5f5-140">Nome del gruppo di gestione della definizione di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="dc5f5-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc5f5-141">-Name</span></span>
<span data-ttu-id="dc5f5-142">Specifica il nome della definizione di criterio rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dc5f5-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="dc5f5-143">-Pre</span></span>
<span data-ttu-id="dc5f5-144">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dc5f5-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc5f5-145">-SubscriptionId</span></span>
<span data-ttu-id="dc5f5-146">ID sottoscrizione della definizione di criterio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="dc5f5-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc5f5-147">-Confirm</span></span>
<span data-ttu-id="dc5f5-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc5f5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc5f5-149">-WhatIf</span></span>
<span data-ttu-id="dc5f5-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc5f5-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc5f5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5f5-152">CommonParameters</span></span>
<span data-ttu-id="dc5f5-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5f5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5f5-154">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5f5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5f5-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc5f5-155">INPUTS</span></span>

## <span data-ttu-id="dc5f5-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc5f5-156">OUTPUTS</span></span>

## <span data-ttu-id="dc5f5-157">Note</span><span class="sxs-lookup"><span data-stu-id="dc5f5-157">NOTES</span></span>

## <span data-ttu-id="dc5f5-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc5f5-158">RELATED LINKS</span></span>

[<span data-ttu-id="dc5f5-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dc5f5-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="dc5f5-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dc5f5-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="dc5f5-161">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dc5f5-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


