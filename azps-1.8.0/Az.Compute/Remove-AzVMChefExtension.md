---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 052082672dd822b78ff6c47abf7710c87c35a746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93851997"
---
# <span data-ttu-id="9e589-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9e589-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="9e589-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e589-102">SYNOPSIS</span></span>
<span data-ttu-id="9e589-103">Rimuove l'estensione dello chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e589-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="9e589-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e589-104">SYNTAX</span></span>

### <span data-ttu-id="9e589-105">Linux</span><span class="sxs-lookup"><span data-stu-id="9e589-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e589-106">Windows</span><span class="sxs-lookup"><span data-stu-id="9e589-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e589-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e589-107">DESCRIPTION</span></span>
<span data-ttu-id="9e589-108">Il cmdlet **Remove-AzVMChefExtension** rimuove l'estensione chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e589-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="9e589-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e589-109">EXAMPLES</span></span>

### <span data-ttu-id="9e589-110">Esempio 1: rimuovere un'estensione dello chef da una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="9e589-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="9e589-111">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="9e589-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="9e589-112">Esempio 2: rimuovere un'estensione dello chef da una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="9e589-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="9e589-113">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="9e589-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="9e589-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e589-114">PARAMETERS</span></span>

### <span data-ttu-id="9e589-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e589-115">-DefaultProfile</span></span>
<span data-ttu-id="9e589-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e589-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e589-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="9e589-117">-Linux</span></span>
<span data-ttu-id="9e589-118">Indica che questo cmdlet è destinato a una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="9e589-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e589-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e589-119">-Name</span></span>
<span data-ttu-id="9e589-120">Specifica il nome dell'estensione dello chef rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e589-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e589-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e589-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e589-122">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e589-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="9e589-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e589-123">-VMName</span></span>
<span data-ttu-id="9e589-124">Specifica il nome di una macchina virtuale per cui questo cmdlet rimuove l'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="9e589-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="9e589-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="9e589-125">-Windows</span></span>
<span data-ttu-id="9e589-126">Indica che questo cmdlet è destinato a una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="9e589-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e589-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e589-127">-Confirm</span></span>
<span data-ttu-id="9e589-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e589-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e589-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e589-129">-WhatIf</span></span>
<span data-ttu-id="9e589-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e589-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e589-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e589-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e589-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e589-132">CommonParameters</span></span>
<span data-ttu-id="9e589-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e589-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e589-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e589-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e589-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e589-135">INPUTS</span></span>

### <span data-ttu-id="9e589-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9e589-136">System.String</span></span>

## <span data-ttu-id="9e589-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e589-137">OUTPUTS</span></span>

### <span data-ttu-id="9e589-138">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9e589-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9e589-139">Note</span><span class="sxs-lookup"><span data-stu-id="9e589-139">NOTES</span></span>

## <span data-ttu-id="9e589-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e589-140">RELATED LINKS</span></span>

[<span data-ttu-id="9e589-141">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9e589-141">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="9e589-142">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9e589-142">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
