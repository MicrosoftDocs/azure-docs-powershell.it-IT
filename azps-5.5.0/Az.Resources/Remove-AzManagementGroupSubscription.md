---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 843a510376e49a1416129d719c141d72ec80df35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201863"
---
# <span data-ttu-id="4fb8e-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="4fb8e-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="4fb8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb8e-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb8e-103">Rimuove una sottoscrizione da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="4fb8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fb8e-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb8e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4fb8e-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb8e-106">Il cmdlet **Remove-AzManagementGroupSubscription** rimuove una sottoscrizione da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="4fb8e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fb8e-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb8e-108">Esempio 1: Rimuovere la sottoscrizione da un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="4fb8e-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="4fb8e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fb8e-109">PARAMETERS</span></span>

### <span data-ttu-id="4fb8e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb8e-110">-DefaultProfile</span></span>
<span data-ttu-id="4fb8e-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb8e-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="4fb8e-112">-GroupName</span></span>
<span data-ttu-id="4fb8e-113">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="4fb8e-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb8e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fb8e-114">-PassThru</span></span>
<span data-ttu-id="4fb8e-115">Ritorno `true` sull'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="4fb8e-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="4fb8e-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fb8e-116">-SubscriptionId</span></span>
<span data-ttu-id="4fb8e-117">ID sottoscrizione dell'abbonamento associato alla gestione</span><span class="sxs-lookup"><span data-stu-id="4fb8e-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="4fb8e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fb8e-118">-Confirm</span></span>
<span data-ttu-id="4fb8e-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb8e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb8e-120">-WhatIf</span></span>
<span data-ttu-id="4fb8e-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fb8e-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb8e-123">CommonParameters</span></span>
<span data-ttu-id="4fb8e-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb8e-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4fb8e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb8e-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4fb8e-126">INPUTS</span></span>

### <span data-ttu-id="4fb8e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4fb8e-127">None</span></span>

## <span data-ttu-id="4fb8e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fb8e-128">OUTPUTS</span></span>

### <span data-ttu-id="4fb8e-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fb8e-129">System.Boolean</span></span>

## <span data-ttu-id="4fb8e-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="4fb8e-130">NOTES</span></span>

## <span data-ttu-id="4fb8e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fb8e-131">RELATED LINKS</span></span>
