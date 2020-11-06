---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519519"
---
# <span data-ttu-id="72239-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72239-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="72239-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72239-102">SYNOPSIS</span></span>
<span data-ttu-id="72239-103">Rimuove un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72239-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72239-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72239-104">SYNTAX</span></span>

### <span data-ttu-id="72239-105">Elenca il gruppo di risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="72239-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="72239-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="72239-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72239-107">Elenca il gruppo di risorse basato sull'ID.</span><span class="sxs-lookup"><span data-stu-id="72239-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72239-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72239-108">DESCRIPTION</span></span>
<span data-ttu-id="72239-109">Il cmdlet **Remove-AzureRmResourceGroup** rimuove un gruppo di risorse Azure e le relative risorse dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="72239-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="72239-110">Per eliminare una risorsa, ma uscire dal gruppo risorse, usare il cmdlet Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="72239-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="72239-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72239-111">EXAMPLES</span></span>

### <span data-ttu-id="72239-112">Esempio 1: rimuovere un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="72239-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="72239-113">Questo comando rimuove il gruppo di risorse ContosoRG01 dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72239-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="72239-114">Il cmdlet richiede la conferma e non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="72239-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="72239-115">Esempio 2: rimuovere un gruppo di risorse senza conferma</span><span class="sxs-lookup"><span data-stu-id="72239-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="72239-116">Questo comando usa il cmdlet Get-AzureRmResourceGroup per ottenere il gruppo di risorse ContosoRG01 e lo passa a **Remove-AzureRmResourceGroup** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="72239-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="72239-117">Il parametro comune *verbose* ottiene le informazioni sullo stato sull'operazione e il parametro *Force* Elimina il messaggio di conferma.</span><span class="sxs-lookup"><span data-stu-id="72239-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="72239-118">Esempio 3: rimuovere tutti i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="72239-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="72239-119">Questo comando usa il cmdlet **Get-AzureRmResourceGroup** per ottenere tutti i gruppi di risorse, quindi li passa a **Remove-AzureRmResourceGroup** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="72239-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="72239-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72239-120">PARAMETERS</span></span>

### <span data-ttu-id="72239-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="72239-121">-ApiVersion</span></span>
<span data-ttu-id="72239-122">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="72239-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="72239-123">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="72239-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="72239-124">-Force</span><span class="sxs-lookup"><span data-stu-id="72239-124">-Force</span></span>
<span data-ttu-id="72239-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="72239-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72239-126">-ID</span><span class="sxs-lookup"><span data-stu-id="72239-126">-Id</span></span>
<span data-ttu-id="72239-127">Specifica l'ID del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="72239-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="72239-128">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="72239-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72239-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="72239-129">-Name</span></span>
<span data-ttu-id="72239-130">Specifica i nomi dei gruppi di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="72239-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="72239-131">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="72239-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72239-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="72239-132">-Pre</span></span>
<span data-ttu-id="72239-133">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="72239-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="72239-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72239-134">-Confirm</span></span>
<span data-ttu-id="72239-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72239-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72239-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72239-136">-WhatIf</span></span>
<span data-ttu-id="72239-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72239-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72239-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72239-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72239-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72239-139">-DefaultProfile</span></span>
<span data-ttu-id="72239-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72239-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72239-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72239-141">CommonParameters</span></span>
<span data-ttu-id="72239-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72239-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72239-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72239-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72239-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72239-144">INPUTS</span></span>

### <span data-ttu-id="72239-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="72239-145">None</span></span>

## <span data-ttu-id="72239-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72239-146">OUTPUTS</span></span>

### <span data-ttu-id="72239-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="72239-147">None</span></span>

## <span data-ttu-id="72239-148">Note</span><span class="sxs-lookup"><span data-stu-id="72239-148">NOTES</span></span>

## <span data-ttu-id="72239-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72239-149">RELATED LINKS</span></span>

[<span data-ttu-id="72239-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72239-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="72239-151">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72239-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="72239-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72239-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


