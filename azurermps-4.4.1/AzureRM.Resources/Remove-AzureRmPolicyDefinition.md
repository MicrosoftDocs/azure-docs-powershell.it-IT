---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687701"
---
# <span data-ttu-id="502a1-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="502a1-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="502a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="502a1-102">SYNOPSIS</span></span>
<span data-ttu-id="502a1-103">Rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="502a1-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="502a1-104">SYNTAX</span></span>

### <span data-ttu-id="502a1-105">Set di parametri nome definizione criteri.</span><span class="sxs-lookup"><span data-stu-id="502a1-105">The policy definition name parameter set.</span></span> <span data-ttu-id="502a1-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="502a1-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="502a1-107">Set di parametri ID definizione criteri.</span><span class="sxs-lookup"><span data-stu-id="502a1-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="502a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="502a1-108">DESCRIPTION</span></span>
<span data-ttu-id="502a1-109">Il cmdlet **Remove-AzureRmPolicyDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="502a1-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="502a1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="502a1-110">EXAMPLES</span></span>

### <span data-ttu-id="502a1-111">Esempio 1: rimuovere la definizione dei criteri in base al nome</span><span class="sxs-lookup"><span data-stu-id="502a1-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="502a1-112">Questo comando rimuove la definizione di criterio specificata.</span><span class="sxs-lookup"><span data-stu-id="502a1-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="502a1-113">Esempio 2: rimuovere la definizione dei criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="502a1-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="502a1-114">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="502a1-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="502a1-115">Il comando lo archivia nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="502a1-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="502a1-116">Il secondo comando rimuove la definizione dei criteri identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="502a1-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="502a1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="502a1-117">PARAMETERS</span></span>

### <span data-ttu-id="502a1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="502a1-118">-ApiVersion</span></span>
<span data-ttu-id="502a1-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="502a1-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="502a1-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="502a1-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="502a1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="502a1-121">-Force</span></span>
<span data-ttu-id="502a1-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="502a1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="502a1-123">-ID</span><span class="sxs-lookup"><span data-stu-id="502a1-123">-Id</span></span>
<span data-ttu-id="502a1-124">Specifica l'ID di risorsa completo per la definizione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="502a1-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="502a1-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="502a1-125">-InformationAction</span></span>
<span data-ttu-id="502a1-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="502a1-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="502a1-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="502a1-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="502a1-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="502a1-128">Continue</span></span>
- <span data-ttu-id="502a1-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="502a1-129">Ignore</span></span>
- <span data-ttu-id="502a1-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="502a1-130">Inquire</span></span>
- <span data-ttu-id="502a1-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="502a1-131">SilentlyContinue</span></span>
- <span data-ttu-id="502a1-132">Stop</span><span class="sxs-lookup"><span data-stu-id="502a1-132">Stop</span></span>
- <span data-ttu-id="502a1-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="502a1-133">Suspend</span></span>

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

### <span data-ttu-id="502a1-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="502a1-134">-InformationVariable</span></span>
<span data-ttu-id="502a1-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="502a1-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="502a1-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="502a1-136">-Name</span></span>
<span data-ttu-id="502a1-137">Specifica il nome della definizione di criterio rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="502a1-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="502a1-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="502a1-138">-Pre</span></span>
<span data-ttu-id="502a1-139">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="502a1-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="502a1-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="502a1-140">-Confirm</span></span>
<span data-ttu-id="502a1-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="502a1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="502a1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="502a1-142">-WhatIf</span></span>
<span data-ttu-id="502a1-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="502a1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="502a1-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="502a1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="502a1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502a1-145">-DefaultProfile</span></span>
<span data-ttu-id="502a1-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="502a1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="502a1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502a1-147">CommonParameters</span></span>
<span data-ttu-id="502a1-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502a1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502a1-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502a1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502a1-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="502a1-150">INPUTS</span></span>

## <span data-ttu-id="502a1-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="502a1-151">OUTPUTS</span></span>

### <span data-ttu-id="502a1-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="502a1-152">System.Boolean</span></span>

## <span data-ttu-id="502a1-153">Note</span><span class="sxs-lookup"><span data-stu-id="502a1-153">NOTES</span></span>

## <span data-ttu-id="502a1-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="502a1-154">RELATED LINKS</span></span>

[<span data-ttu-id="502a1-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="502a1-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="502a1-156">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="502a1-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="502a1-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="502a1-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


