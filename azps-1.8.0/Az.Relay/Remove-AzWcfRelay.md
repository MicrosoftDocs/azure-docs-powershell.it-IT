---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f523f0d1166a40e04ac85344c0fc96640a140bb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677448"
---
# <span data-ttu-id="4de5e-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="4de5e-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="4de5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4de5e-102">SYNOPSIS</span></span>
<span data-ttu-id="4de5e-103">Rimuove WcfRelay dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="4de5e-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="4de5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4de5e-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de5e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4de5e-105">DESCRIPTION</span></span>
<span data-ttu-id="4de5e-106">Il cmdlet **Remove-AzWcfRelay** rimuove WcfRelay dallo spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="4de5e-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="4de5e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4de5e-107">EXAMPLES</span></span>

### <span data-ttu-id="4de5e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4de5e-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="4de5e-109">Rimuove WcfRelay `TestWCFRelay1` dallo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="4de5e-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="4de5e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4de5e-110">PARAMETERS</span></span>

### <span data-ttu-id="4de5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de5e-111">-DefaultProfile</span></span>
<span data-ttu-id="4de5e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4de5e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de5e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4de5e-113">-Name</span></span>
<span data-ttu-id="4de5e-114">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="4de5e-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de5e-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4de5e-115">-Namespace</span></span>
<span data-ttu-id="4de5e-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4de5e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="4de5e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de5e-117">-ResourceGroupName</span></span>
<span data-ttu-id="4de5e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4de5e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="4de5e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4de5e-119">-Confirm</span></span>
<span data-ttu-id="4de5e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4de5e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de5e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de5e-121">-WhatIf</span></span>
<span data-ttu-id="4de5e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4de5e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de5e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4de5e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de5e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de5e-124">CommonParameters</span></span>
<span data-ttu-id="4de5e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de5e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de5e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de5e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de5e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4de5e-127">INPUTS</span></span>

### <span data-ttu-id="4de5e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4de5e-128">System.String</span></span>

## <span data-ttu-id="4de5e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4de5e-129">OUTPUTS</span></span>

### <span data-ttu-id="4de5e-130">System. void</span><span class="sxs-lookup"><span data-stu-id="4de5e-130">System.Void</span></span>

## <span data-ttu-id="4de5e-131">Note</span><span class="sxs-lookup"><span data-stu-id="4de5e-131">NOTES</span></span>

## <span data-ttu-id="4de5e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4de5e-132">RELATED LINKS</span></span>