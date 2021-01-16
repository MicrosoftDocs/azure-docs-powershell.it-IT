---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363747"
---
# <span data-ttu-id="ce531-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ce531-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="ce531-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce531-102">SYNOPSIS</span></span>
<span data-ttu-id="ce531-103">Rimuove un gestore di estensione DSC da una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce531-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="ce531-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce531-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce531-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce531-105">DESCRIPTION</span></span>
<span data-ttu-id="ce531-106">Il cmdlet **Remove-AzVMDscExtension** rimuove un gestore di estensione DSC (per la configurazione di stato) da una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce531-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="ce531-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce531-107">EXAMPLES</span></span>

### <span data-ttu-id="ce531-108">Esempio 1: rimuovere un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="ce531-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="ce531-109">Questo comando rimuove l'estensione denominata DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="ce531-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="ce531-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce531-110">PARAMETERS</span></span>

### <span data-ttu-id="ce531-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce531-111">-DefaultProfile</span></span>
<span data-ttu-id="ce531-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce531-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce531-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce531-113">-Name</span></span>
<span data-ttu-id="ce531-114">Specifica il nome dell'estensione DSC rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce531-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="ce531-115">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è il valore predefinito usato da **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="ce531-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce531-116">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ce531-116">-NoWait</span></span>
<span data-ttu-id="ce531-117">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ce531-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ce531-118">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="ce531-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ce531-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce531-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce531-120">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce531-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ce531-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="ce531-121">-VMName</span></span>
<span data-ttu-id="ce531-122">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="ce531-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce531-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce531-123">-Confirm</span></span>
<span data-ttu-id="ce531-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce531-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce531-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce531-125">-WhatIf</span></span>
<span data-ttu-id="ce531-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce531-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce531-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce531-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce531-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce531-128">CommonParameters</span></span>
<span data-ttu-id="ce531-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce531-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce531-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce531-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce531-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce531-131">INPUTS</span></span>

### <span data-ttu-id="ce531-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ce531-132">System.String</span></span>

## <span data-ttu-id="ce531-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce531-133">OUTPUTS</span></span>

### <span data-ttu-id="ce531-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ce531-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ce531-135">Note</span><span class="sxs-lookup"><span data-stu-id="ce531-135">NOTES</span></span>

## <span data-ttu-id="ce531-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce531-136">RELATED LINKS</span></span>

[<span data-ttu-id="ce531-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ce531-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="ce531-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ce531-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


