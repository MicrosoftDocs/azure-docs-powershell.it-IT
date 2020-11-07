---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 3b7aebf0f0387de728d04ee83fdbce8ee108e207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687359"
---
# <span data-ttu-id="5a675-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="5a675-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="5a675-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a675-102">SYNOPSIS</span></span>
<span data-ttu-id="5a675-103">Rimuove (a) i segreti da un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5a675-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a675-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a675-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a675-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a675-105">DESCRIPTION</span></span>
<span data-ttu-id="5a675-106">Il cmdlet Remove-AzureRmVMSecret rimuove (a) Secret (s) da un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a675-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="5a675-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a675-107">EXAMPLES</span></span>

### <span data-ttu-id="5a675-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a675-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="5a675-109">Rimuove tutti i segreti da una macchina virtuale "VM1" nel gruppo di risorse "RG1" e aggiorna la VM</span><span class="sxs-lookup"><span data-stu-id="5a675-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="5a675-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a675-110">PARAMETERS</span></span>

### <span data-ttu-id="5a675-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a675-111">-DefaultProfile</span></span>
<span data-ttu-id="5a675-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a675-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a675-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5a675-113">-SourceVaultId</span></span>
<span data-ttu-id="5a675-114">Specifica una matrice di ID del Vault di origine rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a675-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a675-115">-VM</span><span class="sxs-lookup"><span data-stu-id="5a675-115">-VM</span></span>
<span data-ttu-id="5a675-116">Specifica la macchina virtuale da cui questo cmdlet rimuove (a) Secret (s).</span><span class="sxs-lookup"><span data-stu-id="5a675-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="5a675-117">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5a675-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a675-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a675-118">-Confirm</span></span>
<span data-ttu-id="5a675-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a675-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a675-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a675-120">-WhatIf</span></span>
<span data-ttu-id="5a675-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a675-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a675-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a675-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a675-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a675-123">CommonParameters</span></span>
<span data-ttu-id="5a675-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a675-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a675-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a675-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a675-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a675-126">INPUTS</span></span>

### <span data-ttu-id="5a675-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5a675-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5a675-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a675-128">OUTPUTS</span></span>

### <span data-ttu-id="5a675-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5a675-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5a675-130">Note</span><span class="sxs-lookup"><span data-stu-id="5a675-130">NOTES</span></span>

## <span data-ttu-id="5a675-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a675-131">RELATED LINKS</span></span>
