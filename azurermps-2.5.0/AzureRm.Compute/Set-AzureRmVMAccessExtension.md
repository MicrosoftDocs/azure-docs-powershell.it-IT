---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 069b98f585d606ade255cfecd223be4a074d8316
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866529"
---
# <span data-ttu-id="49b6c-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="49b6c-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="49b6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="49b6c-103">Aggiunge l'estensione VMAccess a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49b6c-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49b6c-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="49b6c-106">Il cmdlet **set-AzureRmVMAccessExtension** aggiunge l'estensione di VMAccess Virtual Machine Access (VMAccess) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49b6c-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="49b6c-107">L'estensione VMAccess può essere usata per impostare una password temporanea e questo deve essere immediatamente modificato dopo l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="49b6c-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="49b6c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49b6c-108">EXAMPLES</span></span>

### <span data-ttu-id="49b6c-109">Esempio 1: aggiungere un'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="49b6c-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="49b6c-110">Questo comando aggiunge un'estensione VMAccess per la macchina virtuale denominata VirtualMachine07 in ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="49b6c-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="49b6c-111">Il comando specifica la versione del gestore del nome e del tipo per VMAccess.</span><span class="sxs-lookup"><span data-stu-id="49b6c-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="49b6c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49b6c-112">PARAMETERS</span></span>

### <span data-ttu-id="49b6c-113">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="49b6c-113">-Credential</span></span>
<span data-ttu-id="49b6c-114">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="49b6c-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="49b6c-115">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="49b6c-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="49b6c-116">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="49b6c-116">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="49b6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b6c-117">-DefaultProfile</span></span>
<span data-ttu-id="49b6c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49b6c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b6c-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="49b6c-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="49b6c-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="49b6c-120">-ForceRerun</span></span>
<span data-ttu-id="49b6c-121">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="49b6c-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="49b6c-122">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="49b6c-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="49b6c-123">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="49b6c-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="49b6c-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="49b6c-124">-Location</span></span>
<span data-ttu-id="49b6c-125">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49b6c-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="49b6c-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="49b6c-126">-Name</span></span>
<span data-ttu-id="49b6c-127">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b6c-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="49b6c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b6c-128">-ResourceGroupName</span></span>
<span data-ttu-id="49b6c-129">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49b6c-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="49b6c-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="49b6c-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="49b6c-131">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49b6c-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="49b6c-132">Per ottenere la versione, eseguire il cmdlet Get-AzureRmVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="49b6c-132">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="49b6c-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="49b6c-133">-VMName</span></span>
<span data-ttu-id="49b6c-134">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49b6c-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="49b6c-135">Questo cmdlet aggiunge VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="49b6c-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="49b6c-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49b6c-136">-Confirm</span></span>
<span data-ttu-id="49b6c-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b6c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b6c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b6c-138">-WhatIf</span></span>
<span data-ttu-id="49b6c-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49b6c-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="49b6c-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49b6c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b6c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b6c-141">CommonParameters</span></span>
<span data-ttu-id="49b6c-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b6c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b6c-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b6c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b6c-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49b6c-144">INPUTS</span></span>

### <span data-ttu-id="49b6c-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="49b6c-145">None</span></span>
<span data-ttu-id="49b6c-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="49b6c-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49b6c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49b6c-147">OUTPUTS</span></span>

### <span data-ttu-id="49b6c-148">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="49b6c-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="49b6c-149">Note</span><span class="sxs-lookup"><span data-stu-id="49b6c-149">NOTES</span></span>

## <span data-ttu-id="49b6c-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49b6c-150">RELATED LINKS</span></span>

[<span data-ttu-id="49b6c-151">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="49b6c-151">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="49b6c-152">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="49b6c-152">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="49b6c-153">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="49b6c-153">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="49b6c-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="49b6c-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


