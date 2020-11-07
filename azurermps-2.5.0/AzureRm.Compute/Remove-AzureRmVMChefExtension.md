---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: bc8dbd023d8730922614f749f540d182c63237a4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866711"
---
# <span data-ttu-id="0f961-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0f961-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="0f961-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f961-102">SYNOPSIS</span></span>
<span data-ttu-id="0f961-103">Rimuove l'estensione dello chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0f961-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f961-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f961-104">SYNTAX</span></span>

### <span data-ttu-id="0f961-105">Linux</span><span class="sxs-lookup"><span data-stu-id="0f961-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f961-106">Windows</span><span class="sxs-lookup"><span data-stu-id="0f961-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f961-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f961-107">DESCRIPTION</span></span>
<span data-ttu-id="0f961-108">Il cmdlet **Remove-AzureVMChefExtension** rimuove l'estensione chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0f961-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="0f961-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f961-109">EXAMPLES</span></span>

### <span data-ttu-id="0f961-110">Esempio 1: rimuovere un'estensione dello chef da una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="0f961-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="0f961-111">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="0f961-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0f961-112">Esempio 2: rimuovere un'estensione dello chef da una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="0f961-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="0f961-113">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="0f961-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0f961-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f961-114">PARAMETERS</span></span>

### <span data-ttu-id="0f961-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f961-115">-DefaultProfile</span></span>
<span data-ttu-id="0f961-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f961-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f961-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0f961-117">-Linux</span></span>
<span data-ttu-id="0f961-118">Indica che questo cmdlet è destinato a una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="0f961-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f961-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f961-119">-Name</span></span>
<span data-ttu-id="0f961-120">Specifica il nome dell'estensione dello chef rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f961-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f961-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f961-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f961-122">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0f961-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="0f961-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="0f961-123">-VMName</span></span>
<span data-ttu-id="0f961-124">Specifica il nome di una macchina virtuale per cui questo cmdlet rimuove l'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="0f961-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="0f961-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="0f961-125">-Windows</span></span>
<span data-ttu-id="0f961-126">Indica che questo cmdlet è destinato a una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="0f961-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f961-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f961-127">-Confirm</span></span>
<span data-ttu-id="0f961-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f961-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f961-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f961-129">-WhatIf</span></span>
<span data-ttu-id="0f961-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f961-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0f961-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f961-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f961-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f961-132">CommonParameters</span></span>
<span data-ttu-id="0f961-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f961-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f961-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f961-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f961-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f961-135">INPUTS</span></span>

### <span data-ttu-id="0f961-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0f961-136">None</span></span>
<span data-ttu-id="0f961-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0f961-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f961-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f961-138">OUTPUTS</span></span>

### <span data-ttu-id="0f961-139">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0f961-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0f961-140">Note</span><span class="sxs-lookup"><span data-stu-id="0f961-140">NOTES</span></span>

## <span data-ttu-id="0f961-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f961-141">RELATED LINKS</span></span>

[<span data-ttu-id="0f961-142">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0f961-142">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="0f961-143">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0f961-143">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
