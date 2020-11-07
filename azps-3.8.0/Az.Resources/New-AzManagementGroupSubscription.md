---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: a3ef84ef6740eb0d505ff2f9f69670ea83242deb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865009"
---
# <span data-ttu-id="2f55d-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="2f55d-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="2f55d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f55d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f55d-103">Aggiunge una sottoscrizione a un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="2f55d-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="2f55d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f55d-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f55d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f55d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f55d-106">Il cmdlet **New-AzManagementGroupSubscription** aggiunge una sottoscrizione a un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="2f55d-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="2f55d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f55d-107">EXAMPLES</span></span>

### <span data-ttu-id="2f55d-108">Esempio 1: aggiungere una sottoscrizione a un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="2f55d-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="2f55d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f55d-109">PARAMETERS</span></span>

### <span data-ttu-id="2f55d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f55d-110">-DefaultProfile</span></span>
<span data-ttu-id="2f55d-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f55d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f55d-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="2f55d-112">-GroupName</span></span>
<span data-ttu-id="2f55d-113">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="2f55d-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f55d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f55d-114">-PassThru</span></span>
<span data-ttu-id="2f55d-115">Ritorno `true` all'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="2f55d-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="2f55d-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f55d-116">-SubscriptionId</span></span>
<span data-ttu-id="2f55d-117">ID sottoscrizione dell'abbonamento associato alla gestione</span><span class="sxs-lookup"><span data-stu-id="2f55d-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f55d-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2f55d-118">-Confirm</span></span>
<span data-ttu-id="2f55d-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f55d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f55d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f55d-120">-WhatIf</span></span>
<span data-ttu-id="2f55d-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f55d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f55d-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f55d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f55d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f55d-123">CommonParameters</span></span>
<span data-ttu-id="2f55d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f55d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f55d-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f55d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f55d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f55d-126">INPUTS</span></span>

### <span data-ttu-id="2f55d-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2f55d-127">None</span></span>

## <span data-ttu-id="2f55d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f55d-128">OUTPUTS</span></span>

### <span data-ttu-id="2f55d-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f55d-129">System.Boolean</span></span>

## <span data-ttu-id="2f55d-130">Note</span><span class="sxs-lookup"><span data-stu-id="2f55d-130">NOTES</span></span>

## <span data-ttu-id="2f55d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f55d-131">RELATED LINKS</span></span>
