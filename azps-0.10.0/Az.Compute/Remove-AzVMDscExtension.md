---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 69eff38068c379dadc4f3a061cfba4f9cb6539e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863522"
---
# <span data-ttu-id="164b8-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="164b8-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="164b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="164b8-102">SYNOPSIS</span></span>
<span data-ttu-id="164b8-103">Rimuove un gestore di estensione DSC da una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="164b8-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="164b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="164b8-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="164b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="164b8-105">DESCRIPTION</span></span>
<span data-ttu-id="164b8-106">Il cmdlet **Remove-AzVMDscExtension** rimuove un gestore di estensione DSC (per la configurazione di stato) da una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="164b8-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="164b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="164b8-107">EXAMPLES</span></span>

### <span data-ttu-id="164b8-108">Esempio 1: rimuovere un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="164b8-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="164b8-109">Questo comando rimuove l'estensione denominata DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="164b8-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="164b8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="164b8-110">PARAMETERS</span></span>

### <span data-ttu-id="164b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164b8-111">-DefaultProfile</span></span>
<span data-ttu-id="164b8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="164b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="164b8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="164b8-113">-Name</span></span>
<span data-ttu-id="164b8-114">Specifica il nome dell'estensione DSC rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="164b8-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="164b8-115">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è il valore predefinito usato da **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="164b8-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="164b8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="164b8-116">-ResourceGroupName</span></span>
<span data-ttu-id="164b8-117">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="164b8-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="164b8-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="164b8-118">-VMName</span></span>
<span data-ttu-id="164b8-119">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="164b8-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="164b8-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="164b8-120">-Confirm</span></span>
<span data-ttu-id="164b8-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="164b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="164b8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="164b8-122">-WhatIf</span></span>
<span data-ttu-id="164b8-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="164b8-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="164b8-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="164b8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="164b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164b8-125">CommonParameters</span></span>
<span data-ttu-id="164b8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="164b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164b8-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="164b8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164b8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="164b8-128">INPUTS</span></span>

### <span data-ttu-id="164b8-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="164b8-129">None</span></span>
<span data-ttu-id="164b8-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="164b8-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="164b8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="164b8-131">OUTPUTS</span></span>

### <span data-ttu-id="164b8-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="164b8-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="164b8-133">Note</span><span class="sxs-lookup"><span data-stu-id="164b8-133">NOTES</span></span>

## <span data-ttu-id="164b8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="164b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="164b8-135">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="164b8-135">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="164b8-136">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="164b8-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


