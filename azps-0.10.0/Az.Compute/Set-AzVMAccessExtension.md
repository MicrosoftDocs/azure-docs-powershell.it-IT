---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0335a063e810a94e6d557986e682ec4c777e5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863405"
---
# <span data-ttu-id="fb048-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fb048-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="fb048-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb048-102">SYNOPSIS</span></span>
<span data-ttu-id="fb048-103">Aggiunge l'estensione VMAccess a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb048-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="fb048-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb048-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb048-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb048-105">DESCRIPTION</span></span>
<span data-ttu-id="fb048-106">Il cmdlet **set-AzVMAccessExtension** aggiunge l'estensione di VMAccess Virtual Machine Access (VMAccess) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb048-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="fb048-107">L'estensione VMAccess può essere usata per impostare una password temporanea e questo deve essere immediatamente modificato dopo l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="fb048-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="fb048-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb048-108">EXAMPLES</span></span>

### <span data-ttu-id="fb048-109">Esempio 1: aggiungere un'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="fb048-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="fb048-110">Questo comando aggiunge un'estensione VMAccess per la macchina virtuale denominata VirtualMachine07 in ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fb048-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="fb048-111">Il comando specifica la versione del gestore del nome e del tipo per VMAccess.</span><span class="sxs-lookup"><span data-stu-id="fb048-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="fb048-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb048-112">PARAMETERS</span></span>

### <span data-ttu-id="fb048-113">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="fb048-113">-Credential</span></span>
<span data-ttu-id="fb048-114">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="fb048-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="fb048-115">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="fb048-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="fb048-116">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="fb048-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb048-117">-DefaultProfile</span></span>
<span data-ttu-id="fb048-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb048-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb048-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fb048-119">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="fb048-120">-ForceRerun</span></span>
<span data-ttu-id="fb048-121">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="fb048-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="fb048-122">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="fb048-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="fb048-123">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="fb048-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fb048-124">-Location</span></span>
<span data-ttu-id="fb048-125">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb048-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb048-126">-Name</span></span>
<span data-ttu-id="fb048-127">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb048-127">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb048-128">-ResourceGroupName</span></span>
<span data-ttu-id="fb048-129">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb048-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fb048-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="fb048-131">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb048-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="fb048-132">Per ottenere la versione, eseguire il cmdlet Get-AzVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="fb048-132">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="fb048-133">-VMName</span></span>
<span data-ttu-id="fb048-134">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb048-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="fb048-135">Questo cmdlet aggiunge VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fb048-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb048-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb048-136">-Confirm</span></span>
<span data-ttu-id="fb048-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb048-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb048-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb048-138">-WhatIf</span></span>
<span data-ttu-id="fb048-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb048-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fb048-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb048-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb048-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb048-141">CommonParameters</span></span>
<span data-ttu-id="fb048-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb048-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb048-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb048-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb048-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb048-144">INPUTS</span></span>

### <span data-ttu-id="fb048-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fb048-145">None</span></span>
<span data-ttu-id="fb048-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fb048-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb048-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb048-147">OUTPUTS</span></span>

### <span data-ttu-id="fb048-148">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fb048-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fb048-149">Note</span><span class="sxs-lookup"><span data-stu-id="fb048-149">NOTES</span></span>

## <span data-ttu-id="fb048-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb048-150">RELATED LINKS</span></span>

[<span data-ttu-id="fb048-151">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fb048-151">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="fb048-152">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fb048-152">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="fb048-153">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb048-153">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="fb048-154">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="fb048-154">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


