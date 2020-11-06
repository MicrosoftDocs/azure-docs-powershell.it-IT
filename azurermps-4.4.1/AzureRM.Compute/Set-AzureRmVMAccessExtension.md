---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: c77fe7985e91386cad746c61f5849072e0366615
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508628"
---
# <span data-ttu-id="3d3a6-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3d3a6-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="3d3a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3a6-103">Aggiunge l'estensione VMAccess a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d3a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d3a6-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d3a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d3a6-105">DESCRIPTION</span></span>
<span data-ttu-id="3d3a6-106">Il cmdlet **set-AzureRmVMAccessExtension** aggiunge l'estensione della macchina virtuale VMAccess (Virtual Machine Access) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="3d3a6-107">VMAccess può reimpostare il nome utente e la password della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-107">VMAccess can reset the virtual machine user name and password.</span></span>

## <span data-ttu-id="3d3a6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d3a6-108">EXAMPLES</span></span>

### <span data-ttu-id="3d3a6-109">Esempio 1: aggiungere un'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="3d3a6-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="3d3a6-110">Questo comando aggiunge un'estensione VMAccess per la macchina virtuale denominata VirtualMachine07 in ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="3d3a6-111">Il comando specifica la versione del gestore del nome e del tipo per VMAccess.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="3d3a6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d3a6-112">PARAMETERS</span></span>

### <span data-ttu-id="3d3a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3a6-113">-DefaultProfile</span></span>
<span data-ttu-id="3d3a6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d3a6-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3d3a6-115">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="3d3a6-116">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3d3a6-116">-ForceRerun</span></span>
<span data-ttu-id="3d3a6-117">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-117">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="3d3a6-118">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-118">The value can be any string different from the current value.</span></span>

<span data-ttu-id="3d3a6-119">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-119">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="3d3a6-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3d3a6-120">-Location</span></span>
<span data-ttu-id="3d3a6-121">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-121">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="3d3a6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d3a6-122">-Name</span></span>
<span data-ttu-id="3d3a6-123">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-123">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3d3a6-124">-Password</span><span class="sxs-lookup"><span data-stu-id="3d3a6-124">-Password</span></span>
<span data-ttu-id="3d3a6-125">Specifica la nuova password della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-125">Specifies the new password of the virtual machine.</span></span>

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

### <span data-ttu-id="3d3a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d3a6-127">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3d3a6-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3d3a6-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="3d3a6-129">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="3d3a6-130">Per ottenere la versione, eseguire il cmdlet Get-AzureRmVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="3d3a6-130">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="3d3a6-131">-UserName</span><span class="sxs-lookup"><span data-stu-id="3d3a6-131">-UserName</span></span>
<span data-ttu-id="3d3a6-132">Specifica il nuovo nome utente per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-132">Specifies the new user name for the virtual machine.</span></span>

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

### <span data-ttu-id="3d3a6-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="3d3a6-133">-VMName</span></span>
<span data-ttu-id="3d3a6-134">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3d3a6-135">Questo cmdlet aggiunge VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d3a6-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3d3a6-136">-Confirm</span></span>
<span data-ttu-id="3d3a6-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d3a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d3a6-138">-WhatIf</span></span>
<span data-ttu-id="3d3a6-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3d3a6-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d3a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3a6-141">CommonParameters</span></span>
<span data-ttu-id="3d3a6-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d3a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3a6-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3a6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3a6-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d3a6-144">INPUTS</span></span>

## <span data-ttu-id="3d3a6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d3a6-145">OUTPUTS</span></span>

## <span data-ttu-id="3d3a6-146">Note</span><span class="sxs-lookup"><span data-stu-id="3d3a6-146">NOTES</span></span>

## <span data-ttu-id="3d3a6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d3a6-147">RELATED LINKS</span></span>

[<span data-ttu-id="3d3a6-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3d3a6-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3d3a6-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3d3a6-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3d3a6-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3d3a6-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="3d3a6-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3d3a6-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


