---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: caa0baf8e26ea2cec94a59bd2a86e6394b4ade91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855210"
---
# <span data-ttu-id="4edb4-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="4edb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4edb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4edb4-103">Imposta i tag per un PublicIpPrefix esistente</span><span class="sxs-lookup"><span data-stu-id="4edb4-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="4edb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4edb4-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4edb4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4edb4-105">DESCRIPTION</span></span>
<span data-ttu-id="4edb4-106">Il cmdlet **set-AzPublicIpPrefix** imposta i tag per un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="4edb4-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="4edb4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4edb4-107">EXAMPLES</span></span>

### <span data-ttu-id="4edb4-108">Impostare i tag per il prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="4edb4-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="4edb4-109">Il primo comando ottiene un prefisso IP pubblico esistente, il secondo comando imposta la proprietà Tags e il terzo comando Aggiorna l'oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="4edb4-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="4edb4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4edb4-110">PARAMETERS</span></span>

### <span data-ttu-id="4edb4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4edb4-111">-AsJob</span></span>
<span data-ttu-id="4edb4-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4edb4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4edb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4edb4-113">-DefaultProfile</span></span>
<span data-ttu-id="4edb4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4edb4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4edb4-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-115">-PublicIpPrefix</span></span>
<span data-ttu-id="4edb4-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4edb4-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4edb4-117">-Confirm</span></span>
<span data-ttu-id="4edb4-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4edb4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4edb4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4edb4-119">-WhatIf</span></span>
<span data-ttu-id="4edb4-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4edb4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4edb4-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4edb4-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4edb4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4edb4-122">CommonParameters</span></span>
<span data-ttu-id="4edb4-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4edb4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4edb4-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4edb4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4edb4-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4edb4-125">INPUTS</span></span>

### <span data-ttu-id="4edb4-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="4edb4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4edb4-127">OUTPUTS</span></span>

### <span data-ttu-id="4edb4-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="4edb4-129">Note</span><span class="sxs-lookup"><span data-stu-id="4edb4-129">NOTES</span></span>

## <span data-ttu-id="4edb4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4edb4-130">RELATED LINKS</span></span>

[<span data-ttu-id="4edb4-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="4edb4-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="4edb4-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4edb4-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
