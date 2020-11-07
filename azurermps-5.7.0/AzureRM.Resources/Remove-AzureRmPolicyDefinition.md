---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685604"
---
# <span data-ttu-id="bdfe3-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdfe3-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="bdfe3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdfe3-102">SYNOPSIS</span></span>
<span data-ttu-id="bdfe3-103">Rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdfe3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdfe3-104">SYNTAX</span></span>

### <span data-ttu-id="bdfe3-105">RemoveByPolicyDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdfe3-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdfe3-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bdfe3-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdfe3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdfe3-107">DESCRIPTION</span></span>
<span data-ttu-id="bdfe3-108">Il cmdlet **Remove-AzureRmPolicyDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="bdfe3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdfe3-109">EXAMPLES</span></span>

### <span data-ttu-id="bdfe3-110">Esempio 1: rimuovere la definizione dei criteri in base al nome</span><span class="sxs-lookup"><span data-stu-id="bdfe3-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="bdfe3-111">Questo comando rimuove la definizione di criterio specificata.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="bdfe3-112">Esempio 2: rimuovere la definizione dei criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="bdfe3-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="bdfe3-113">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="bdfe3-114">Il comando lo archivia nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="bdfe3-115">Il secondo comando rimuove la definizione dei criteri identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="bdfe3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdfe3-116">PARAMETERS</span></span>

### <span data-ttu-id="bdfe3-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bdfe3-117">-ApiVersion</span></span>
<span data-ttu-id="bdfe3-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bdfe3-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdfe3-120">-DefaultProfile</span></span>
<span data-ttu-id="bdfe3-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bdfe3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bdfe3-122">-Force</span></span>
<span data-ttu-id="bdfe3-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-124">-ID</span><span class="sxs-lookup"><span data-stu-id="bdfe3-124">-Id</span></span>
<span data-ttu-id="bdfe3-125">Specifica l'ID di risorsa completo per la definizione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bdfe3-126">-InformationAction</span></span>
<span data-ttu-id="bdfe3-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bdfe3-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bdfe3-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bdfe3-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="bdfe3-129">Continue</span></span>
- <span data-ttu-id="bdfe3-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="bdfe3-130">Ignore</span></span>
- <span data-ttu-id="bdfe3-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="bdfe3-131">Inquire</span></span>
- <span data-ttu-id="bdfe3-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bdfe3-132">SilentlyContinue</span></span>
- <span data-ttu-id="bdfe3-133">Stop</span><span class="sxs-lookup"><span data-stu-id="bdfe3-133">Stop</span></span>
- <span data-ttu-id="bdfe3-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="bdfe3-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bdfe3-135">-InformationVariable</span></span>
<span data-ttu-id="bdfe3-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdfe3-137">-Name</span></span>
<span data-ttu-id="bdfe3-138">Specifica il nome della definizione di criterio rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="bdfe3-139">-Pre</span></span>
<span data-ttu-id="bdfe3-140">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bdfe3-141">-Confirm</span></span>
<span data-ttu-id="bdfe3-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdfe3-143">-WhatIf</span></span>
<span data-ttu-id="bdfe3-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdfe3-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfe3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdfe3-146">CommonParameters</span></span>
<span data-ttu-id="bdfe3-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdfe3-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdfe3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdfe3-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdfe3-149">INPUTS</span></span>

### <span data-ttu-id="bdfe3-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bdfe3-150">None</span></span>
<span data-ttu-id="bdfe3-151">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bdfe3-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bdfe3-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdfe3-152">OUTPUTS</span></span>

### <span data-ttu-id="bdfe3-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdfe3-153">System.Boolean</span></span>

## <span data-ttu-id="bdfe3-154">Note</span><span class="sxs-lookup"><span data-stu-id="bdfe3-154">NOTES</span></span>

## <span data-ttu-id="bdfe3-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdfe3-155">RELATED LINKS</span></span>

[<span data-ttu-id="bdfe3-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdfe3-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bdfe3-157">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdfe3-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bdfe3-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdfe3-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


