---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684700"
---
# <span data-ttu-id="ec035-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ec035-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="ec035-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec035-102">SYNOPSIS</span></span>
<span data-ttu-id="ec035-103">Aggiunge l'estensione VMAccess a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ec035-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="ec035-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec035-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec035-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec035-105">DESCRIPTION</span></span>
<span data-ttu-id="ec035-106">Il cmdlet **set-AzVMAccessExtension** aggiunge l'estensione di VMAccess Virtual Machine Access (VMAccess) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ec035-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="ec035-107">L'estensione VMAccess può essere usata per impostare una password temporanea e questo deve essere immediatamente modificato dopo l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="ec035-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="ec035-108">Questa operazione non è supportata nei controller di dominio Windows.</span><span class="sxs-lookup"><span data-stu-id="ec035-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="ec035-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec035-109">EXAMPLES</span></span>

### <span data-ttu-id="ec035-110">Esempio 1: aggiungere un'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="ec035-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="ec035-111">Questo comando aggiunge un'estensione VMAccess per la macchina virtuale denominata VirtualMachine07 in ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ec035-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="ec035-112">Il comando specifica la versione del gestore del nome e del tipo per VMAccess.</span><span class="sxs-lookup"><span data-stu-id="ec035-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="ec035-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec035-113">PARAMETERS</span></span>

### <span data-ttu-id="ec035-114">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="ec035-114">-Credential</span></span>
<span data-ttu-id="ec035-115">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="ec035-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="ec035-116">Se si digita un nome diverso da quello dell'account di amministratore locale corrente nella propria VM, l'estensione VMAccess aggiungerà un account di amministratore locale con tale nome e la password specificata verrà assegnata all'account.</span><span class="sxs-lookup"><span data-stu-id="ec035-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="ec035-117">Se l'account di amministratore locale della VM esiste, la password verrà reimpostata e, se l'account è disabilitato, l'estensione VMAccess lo Abilita.</span><span class="sxs-lookup"><span data-stu-id="ec035-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="ec035-118">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="ec035-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ec035-119">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ec035-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec035-120">-DefaultProfile</span></span>
<span data-ttu-id="ec035-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec035-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec035-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ec035-122">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ec035-123">-ForceRerun</span></span>
<span data-ttu-id="ec035-124">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ec035-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ec035-125">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="ec035-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="ec035-126">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="ec035-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ec035-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ec035-127">-Location</span></span>
<span data-ttu-id="ec035-128">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ec035-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ec035-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec035-129">-Name</span></span>
<span data-ttu-id="ec035-130">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec035-130">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec035-131">-ResourceGroupName</span></span>
<span data-ttu-id="ec035-132">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ec035-132">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ec035-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="ec035-134">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ec035-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ec035-135">Per ottenere la versione, eseguire il cmdlet Get-AzVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="ec035-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="ec035-136">Il valore di typeHandlerVersion deve essere 2,0 o maggiore, poiché la versione 1 è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ec035-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="ec035-137">-VMName</span></span>
<span data-ttu-id="ec035-138">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ec035-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ec035-139">Questo cmdlet aggiunge VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ec035-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec035-140">-Confirm</span></span>
<span data-ttu-id="ec035-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec035-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec035-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec035-142">-WhatIf</span></span>
<span data-ttu-id="ec035-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec035-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec035-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec035-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec035-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec035-145">CommonParameters</span></span>
<span data-ttu-id="ec035-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec035-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec035-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec035-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec035-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec035-148">INPUTS</span></span>

### <span data-ttu-id="ec035-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="ec035-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ec035-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ec035-150">System.String</span></span>

### <span data-ttu-id="ec035-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec035-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec035-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec035-152">OUTPUTS</span></span>

### <span data-ttu-id="ec035-153">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ec035-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ec035-154">Note</span><span class="sxs-lookup"><span data-stu-id="ec035-154">NOTES</span></span>

## <span data-ttu-id="ec035-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec035-155">RELATED LINKS</span></span>

[<span data-ttu-id="ec035-156">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ec035-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="ec035-157">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ec035-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="ec035-158">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ec035-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="ec035-159">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ec035-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


