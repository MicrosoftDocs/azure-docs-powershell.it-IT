---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 1f549f86d2fd9313b8d69f02ebcaeccf2f248d4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019720"
---
# <span data-ttu-id="bd5f8-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="bd5f8-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="bd5f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5f8-103">Rimuove un abbonamento da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="bd5f8-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="bd5f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd5f8-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd5f8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd5f8-105">DESCRIPTION</span></span>
<span data-ttu-id="bd5f8-106">Il cmdlet **Remove-AzManagementGroupSubscription** rimuove un abbonamento da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="bd5f8-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="bd5f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd5f8-107">EXAMPLES</span></span>

### <span data-ttu-id="bd5f8-108">Esempio 1-rimuovere l'abbonamento da un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="bd5f8-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="bd5f8-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd5f8-109">PARAMETERS</span></span>

### <span data-ttu-id="bd5f8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd5f8-110">-DefaultProfile</span></span>
<span data-ttu-id="bd5f8-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd5f8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd5f8-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="bd5f8-112">-GroupName</span></span>
<span data-ttu-id="bd5f8-113">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="bd5f8-113">Management Group Id</span></span>

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

### <span data-ttu-id="bd5f8-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd5f8-114">-PassThru</span></span>
<span data-ttu-id="bd5f8-115">Ritorno `true` all'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="bd5f8-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="bd5f8-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd5f8-116">-SubscriptionId</span></span>
<span data-ttu-id="bd5f8-117">ID sottoscrizione dell'abbonamento associato alla gestione</span><span class="sxs-lookup"><span data-stu-id="bd5f8-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="bd5f8-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bd5f8-118">-Confirm</span></span>
<span data-ttu-id="bd5f8-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd5f8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd5f8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd5f8-120">-WhatIf</span></span>
<span data-ttu-id="bd5f8-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd5f8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd5f8-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd5f8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd5f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd5f8-123">CommonParameters</span></span>
<span data-ttu-id="bd5f8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd5f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd5f8-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd5f8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd5f8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd5f8-126">INPUTS</span></span>

### <span data-ttu-id="bd5f8-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd5f8-127">None</span></span>

## <span data-ttu-id="bd5f8-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd5f8-128">OUTPUTS</span></span>

### <span data-ttu-id="bd5f8-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd5f8-129">System.Boolean</span></span>

## <span data-ttu-id="bd5f8-130">Note</span><span class="sxs-lookup"><span data-stu-id="bd5f8-130">NOTES</span></span>

## <span data-ttu-id="bd5f8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd5f8-131">RELATED LINKS</span></span>
