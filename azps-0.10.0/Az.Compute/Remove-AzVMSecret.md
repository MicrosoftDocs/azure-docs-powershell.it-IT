---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: da904e6dfbf9d85319636b3bc6ff5ced5f0b2973
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863514"
---
# <span data-ttu-id="60d13-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="60d13-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="60d13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60d13-102">SYNOPSIS</span></span>
<span data-ttu-id="60d13-103">Rimuove (a) i segreti da un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="60d13-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="60d13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60d13-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60d13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d13-105">DESCRIPTION</span></span>
<span data-ttu-id="60d13-106">Il cmdlet Remove-AzVMSecret rimuove (a) Secret (s) da un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="60d13-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="60d13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60d13-107">EXAMPLES</span></span>

### <span data-ttu-id="60d13-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60d13-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="60d13-109">Rimuove tutti i segreti da una macchina virtuale "VM1" nel gruppo di risorse "RG1" e aggiorna la VM</span><span class="sxs-lookup"><span data-stu-id="60d13-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="60d13-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60d13-110">PARAMETERS</span></span>

### <span data-ttu-id="60d13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d13-111">-DefaultProfile</span></span>
<span data-ttu-id="60d13-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60d13-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60d13-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="60d13-113">-SourceVaultId</span></span>
<span data-ttu-id="60d13-114">Specifica una matrice di ID del Vault di origine rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60d13-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d13-115">-VM</span><span class="sxs-lookup"><span data-stu-id="60d13-115">-VM</span></span>
<span data-ttu-id="60d13-116">Specifica la macchina virtuale da cui questo cmdlet rimuove (a) Secret (s).</span><span class="sxs-lookup"><span data-stu-id="60d13-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="60d13-117">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="60d13-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60d13-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60d13-118">-Confirm</span></span>
<span data-ttu-id="60d13-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60d13-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60d13-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60d13-120">-WhatIf</span></span>
<span data-ttu-id="60d13-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60d13-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60d13-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60d13-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60d13-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d13-123">CommonParameters</span></span>
<span data-ttu-id="60d13-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d13-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d13-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60d13-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d13-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60d13-126">INPUTS</span></span>

### <span data-ttu-id="60d13-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60d13-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="60d13-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60d13-128">OUTPUTS</span></span>

### <span data-ttu-id="60d13-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60d13-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="60d13-130">Note</span><span class="sxs-lookup"><span data-stu-id="60d13-130">NOTES</span></span>

## <span data-ttu-id="60d13-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60d13-131">RELATED LINKS</span></span>

