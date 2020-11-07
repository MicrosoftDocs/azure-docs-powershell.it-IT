---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 97ddf35b453b324cf04309afd3a90be185d43224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686854"
---
# <span data-ttu-id="5b1d2-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b1d2-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="5b1d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1d2-103">Rimuove l'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b1d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b1d2-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b1d2-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1d2-106">Il cmdlet **Remove-AzureRmVMAccessExtension** rimuove l'estensione della macchina virtuale VMAccess (Virtual Machine Access) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="5b1d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b1d2-107">EXAMPLES</span></span>

## <span data-ttu-id="5b1d2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b1d2-108">PARAMETERS</span></span>

### <span data-ttu-id="5b1d2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1d2-109">-DefaultProfile</span></span>
<span data-ttu-id="5b1d2-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b1d2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5b1d2-111">-Force</span></span>
<span data-ttu-id="5b1d2-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b1d2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b1d2-113">-Name</span></span>
<span data-ttu-id="5b1d2-114">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1d2-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b1d2-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5b1d2-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b1d2-117">-VMName</span></span>
<span data-ttu-id="5b1d2-118">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5b1d2-119">Questo cmdlet consente di rimuovere VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b1d2-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b1d2-120">-Confirm</span></span>
<span data-ttu-id="5b1d2-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1d2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1d2-122">-WhatIf</span></span>
<span data-ttu-id="5b1d2-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5b1d2-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1d2-125">CommonParameters</span></span>
<span data-ttu-id="5b1d2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1d2-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b1d2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1d2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b1d2-128">INPUTS</span></span>

## <span data-ttu-id="5b1d2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b1d2-129">OUTPUTS</span></span>

## <span data-ttu-id="5b1d2-130">Note</span><span class="sxs-lookup"><span data-stu-id="5b1d2-130">NOTES</span></span>

## <span data-ttu-id="5b1d2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b1d2-131">RELATED LINKS</span></span>

[<span data-ttu-id="5b1d2-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b1d2-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5b1d2-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b1d2-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5b1d2-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b1d2-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
