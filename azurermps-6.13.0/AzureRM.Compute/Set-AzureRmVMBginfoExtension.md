---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: ac2a4e4e7d05aa23a5870f8a07ded2c7a43fcdae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509267"
---
# <span data-ttu-id="50db3-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="50db3-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="50db3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50db3-102">SYNOPSIS</span></span>
<span data-ttu-id="50db3-103">Aggiunge l'estensione BGInfo a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="50db3-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50db3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50db3-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50db3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50db3-105">DESCRIPTION</span></span>
<span data-ttu-id="50db3-106">Il cmdlet **set-AzureRmVMBGInfoExtension** aggiunge l'estensione BGInfo a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="50db3-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="50db3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50db3-107">EXAMPLES</span></span>

### <span data-ttu-id="50db3-108">Esempio 1: aggiungere l'estensione BGInfo per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="50db3-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="50db3-109">Questo comando aggiunge l'estensione BGInfo alla macchina virtuale denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="50db3-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="50db3-110">Il comando specifica il gruppo di risorse e la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="50db3-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="50db3-111">Il comando specifica il nome e la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="50db3-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="50db3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50db3-112">PARAMETERS</span></span>

### <span data-ttu-id="50db3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50db3-113">-DefaultProfile</span></span>
<span data-ttu-id="50db3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50db3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50db3-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="50db3-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="50db3-116">Indica che questo cmdlet impedisce all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="50db3-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="50db3-117">Per impostazione predefinita, questo cmdlet consente all'agente guest di aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="50db3-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="50db3-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="50db3-118">-ForceRerun</span></span>
<span data-ttu-id="50db3-119">Specifica che l'estensione deve essere eseguita di nuovo con le stesse impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="50db3-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="50db3-120">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="50db3-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="50db3-121">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="50db3-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="50db3-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="50db3-122">-Location</span></span>
<span data-ttu-id="50db3-123">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="50db3-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="50db3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="50db3-124">-Name</span></span>
<span data-ttu-id="50db3-125">Specifica il nome dell'estensione BGInfo che questo cmdlet aggiunge a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="50db3-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="50db3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50db3-126">-ResourceGroupName</span></span>
<span data-ttu-id="50db3-127">Specifica il nome del gruppo di risorse della macchina virtuale a cui questo cmdlet aggiunge un'estensione.</span><span class="sxs-lookup"><span data-stu-id="50db3-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="50db3-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="50db3-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="50db3-129">Specifica la versione dell'estensione aggiunta da questo cmdlet alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="50db3-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="50db3-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="50db3-130">-VMName</span></span>
<span data-ttu-id="50db3-131">Specifica il nome della macchina virtuale a cui questo cmdlet aggiunge l'estensione BGInfo.</span><span class="sxs-lookup"><span data-stu-id="50db3-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="50db3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50db3-132">-Confirm</span></span>
<span data-ttu-id="50db3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50db3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50db3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50db3-134">-WhatIf</span></span>
<span data-ttu-id="50db3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50db3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50db3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50db3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50db3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50db3-137">CommonParameters</span></span>
<span data-ttu-id="50db3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50db3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50db3-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50db3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50db3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50db3-140">INPUTS</span></span>

### <span data-ttu-id="50db3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="50db3-141">System.String</span></span>

### <span data-ttu-id="50db3-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="50db3-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="50db3-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50db3-143">OUTPUTS</span></span>

### <span data-ttu-id="50db3-144">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="50db3-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="50db3-145">Note</span><span class="sxs-lookup"><span data-stu-id="50db3-145">NOTES</span></span>

## <span data-ttu-id="50db3-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50db3-146">RELATED LINKS</span></span>