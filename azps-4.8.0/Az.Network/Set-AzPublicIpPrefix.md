---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188378"
---
# <span data-ttu-id="91968-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="91968-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91968-102">SYNOPSIS</span></span>
<span data-ttu-id="91968-103">Imposta i tag per un PublicIpPrefix esistente</span><span class="sxs-lookup"><span data-stu-id="91968-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="91968-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91968-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91968-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91968-105">DESCRIPTION</span></span>
<span data-ttu-id="91968-106">Il cmdlet **set-AzPublicIpPrefix** imposta i tag per un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="91968-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="91968-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91968-107">EXAMPLES</span></span>

### <span data-ttu-id="91968-108">Impostare i tag per il prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="91968-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="91968-109">Il primo comando ottiene un prefisso IP pubblico esistente, il secondo comando imposta la proprietà Tags e il terzo comando Aggiorna l'oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="91968-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="91968-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91968-110">PARAMETERS</span></span>

### <span data-ttu-id="91968-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91968-111">-AsJob</span></span>
<span data-ttu-id="91968-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="91968-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91968-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91968-113">-DefaultProfile</span></span>
<span data-ttu-id="91968-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91968-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91968-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-115">-PublicIpPrefix</span></span>
<span data-ttu-id="91968-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="91968-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91968-117">-Confirm</span></span>
<span data-ttu-id="91968-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91968-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91968-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91968-119">-WhatIf</span></span>
<span data-ttu-id="91968-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91968-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91968-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91968-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91968-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91968-122">CommonParameters</span></span>
<span data-ttu-id="91968-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91968-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91968-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91968-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91968-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91968-125">INPUTS</span></span>

### <span data-ttu-id="91968-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="91968-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91968-127">OUTPUTS</span></span>

### <span data-ttu-id="91968-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="91968-129">Note</span><span class="sxs-lookup"><span data-stu-id="91968-129">NOTES</span></span>

## <span data-ttu-id="91968-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91968-130">RELATED LINKS</span></span>

[<span data-ttu-id="91968-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="91968-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="91968-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="91968-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)