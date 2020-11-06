---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509963"
---
# <span data-ttu-id="7f3fa-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="7f3fa-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="7f3fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3fa-103">Aggiunge l'estensione BGInfo a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f3fa-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f3fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f3fa-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3fa-106">Il cmdlet **set-AzureRmVMBGInfoExtension** aggiunge l'estensione BGInfo a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="7f3fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f3fa-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3fa-108">Esempio 1: aggiungere l'estensione BGInfo a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7f3fa-108">Example 1: Add the BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
<span data-ttu-id="7f3fa-109">Questo comando aggiunge l'estensione BGInfo a una macchina virtuale denominata ContosoVM nel gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-109">This command adds the BGInfo extension to a virtual machine named ContosoVM in the resource group ContosoRG.</span></span>

### <span data-ttu-id="7f3fa-110">Esempio 2: aggiungere una versione specifica dell'estensione BGInfo a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7f3fa-110">Example 2: Add a specific version of BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="7f3fa-111">Questo comando aggiunge l'estensione BGInfo alla macchina virtuale denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-111">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="7f3fa-112">Il comando specifica il gruppo di risorse e la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-112">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="7f3fa-113">Il comando specifica il nome e la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-113">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="7f3fa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f3fa-114">PARAMETERS</span></span>

### <span data-ttu-id="7f3fa-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7f3fa-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7f3fa-116">Indica che questo cmdlet impedisce all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="7f3fa-117">Per impostazione predefinita, questo cmdlet consente all'agente guest di aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="7f3fa-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="7f3fa-118">-ForceRerun</span></span>
<span data-ttu-id="7f3fa-119">Specifica che l'estensione deve essere eseguita di nuovo con le stesse impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="7f3fa-120">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="7f3fa-121">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="7f3fa-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7f3fa-122">-Location</span></span>
<span data-ttu-id="7f3fa-123">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7f3fa-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f3fa-124">-Name</span></span>
<span data-ttu-id="7f3fa-125">Specifica il nome dell'estensione BGInfo che questo cmdlet aggiunge a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="7f3fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f3fa-127">Specifica il nome del gruppo di risorse della macchina virtuale a cui questo cmdlet aggiunge un'estensione.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="7f3fa-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7f3fa-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="7f3fa-129">Specifica la versione dell'estensione aggiunta da questo cmdlet alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="7f3fa-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="7f3fa-130">-VMName</span></span>
<span data-ttu-id="7f3fa-131">Specifica il nome della macchina virtuale a cui questo cmdlet aggiunge l'estensione BGInfo.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="7f3fa-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f3fa-132">-Confirm</span></span>
<span data-ttu-id="7f3fa-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f3fa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f3fa-134">-WhatIf</span></span>
<span data-ttu-id="7f3fa-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7f3fa-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f3fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3fa-137">CommonParameters</span></span>
<span data-ttu-id="7f3fa-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3fa-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3fa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3fa-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f3fa-140">INPUTS</span></span>

### <span data-ttu-id="7f3fa-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7f3fa-141">None</span></span>
<span data-ttu-id="7f3fa-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7f3fa-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f3fa-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f3fa-143">OUTPUTS</span></span>

## <span data-ttu-id="7f3fa-144">Note</span><span class="sxs-lookup"><span data-stu-id="7f3fa-144">NOTES</span></span>

## <span data-ttu-id="7f3fa-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f3fa-145">RELATED LINKS</span></span>

