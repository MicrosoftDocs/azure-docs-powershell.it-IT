---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030873"
---
# <span data-ttu-id="c4b20-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c4b20-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="c4b20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4b20-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b20-103">Rimuove gli oggetti ruolo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4b20-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="c4b20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4b20-104">SYNTAX</span></span>

### <span data-ttu-id="c4b20-105">FromVMRoleObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4b20-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4b20-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="c4b20-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4b20-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4b20-107">DESCRIPTION</span></span>
<span data-ttu-id="c4b20-108">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="c4b20-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c4b20-109">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b20-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c4b20-110">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c4b20-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c4b20-111">Il cmdlet **Remove-WAPackVMRole** rimuove gli oggetti Role della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4b20-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="c4b20-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4b20-112">EXAMPLES</span></span>

### <span data-ttu-id="c4b20-113">Esempio 1: rimuovere un ruolo macchina virtuale (creato con il portale WAP)</span><span class="sxs-lookup"><span data-stu-id="c4b20-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="c4b20-114">Il primo comando ottiene il ruolo della macchina virtuale denominato ContosoVMRole01 usando il cmdlet **Get-WAPackVMRole** e quindi archivia tale oggetto nella variabile $VMRole.</span><span class="sxs-lookup"><span data-stu-id="c4b20-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="c4b20-115">Il secondo comando rimuove il ruolo della macchina virtuale archiviato in $VMRole.</span><span class="sxs-lookup"><span data-stu-id="c4b20-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="c4b20-116">Il comando richiede la conferma. Supponendo che il ruolo della macchina virtuale sia stato creato usando il portale WAP, non è necessario specificare il nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c4b20-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="c4b20-117">Esempio 2: rimuovere un ruolo macchina virtuale creato dopo la creazione manuale di un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="c4b20-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="c4b20-118">Il primo comando ottiene il ruolo della macchina virtuale denominato "ContosoVMRole02" usando il cmdlet **Get-WAPackVMRole** e quindi archivia tale oggetto nella variabile $VMRole.</span><span class="sxs-lookup"><span data-stu-id="c4b20-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="c4b20-119">Il secondo comando rimuove il ruolo della macchina virtuale archiviato in $VMRole.</span><span class="sxs-lookup"><span data-stu-id="c4b20-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="c4b20-120">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="c4b20-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="c4b20-121">Supponendo che il ruolo della macchina virtuale non sia stato creato usando il portale, l'utente deve specificare il nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c4b20-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="c4b20-122">In questo caso denominato "ContosoCloudService02".</span><span class="sxs-lookup"><span data-stu-id="c4b20-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="c4b20-123">Esempio 3: rimuovere un ruolo macchina virtuale senza conferma</span><span class="sxs-lookup"><span data-stu-id="c4b20-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="c4b20-124">Il primo comando ottiene il servizio cloud denominato ContosoVMRole03 usando il cmdlet **Get-WAPackVMRole** e quindi archivia tale oggetto nella variabile $VMRole.</span><span class="sxs-lookup"><span data-stu-id="c4b20-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="c4b20-125">Il secondo comando rimuove il ruolo della macchina virtuale archiviato in $VMRole.</span><span class="sxs-lookup"><span data-stu-id="c4b20-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="c4b20-126">Questo comando include il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="c4b20-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="c4b20-127">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c4b20-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c4b20-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4b20-128">PARAMETERS</span></span>

### <span data-ttu-id="c4b20-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="c4b20-129">-CloudServiceName</span></span>
<span data-ttu-id="c4b20-130">Specifica il nome del servizio cloud del ruolo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4b20-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b20-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c4b20-131">-Force</span></span>
<span data-ttu-id="c4b20-132">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c4b20-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4b20-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4b20-133">-PassThru</span></span>
<span data-ttu-id="c4b20-134">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c4b20-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c4b20-135">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c4b20-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c4b20-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="c4b20-136">-Profile</span></span>
<span data-ttu-id="c4b20-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b20-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4b20-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c4b20-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b20-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="c4b20-139">-VMRole</span></span>
<span data-ttu-id="c4b20-140">Specifica un ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4b20-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="c4b20-141">Per ottenere un ruolo di macchina virtuale, usare il cmdlet **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="c4b20-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b20-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4b20-142">-Confirm</span></span>
<span data-ttu-id="c4b20-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b20-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b20-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b20-144">-WhatIf</span></span>
<span data-ttu-id="c4b20-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4b20-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4b20-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4b20-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b20-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b20-147">CommonParameters</span></span>
<span data-ttu-id="c4b20-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b20-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b20-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b20-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b20-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4b20-150">INPUTS</span></span>

## <span data-ttu-id="c4b20-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4b20-151">OUTPUTS</span></span>

## <span data-ttu-id="c4b20-152">Note</span><span class="sxs-lookup"><span data-stu-id="c4b20-152">NOTES</span></span>

## <span data-ttu-id="c4b20-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4b20-153">RELATED LINKS</span></span>

[<span data-ttu-id="c4b20-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c4b20-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="c4b20-155">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c4b20-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="c4b20-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c4b20-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


