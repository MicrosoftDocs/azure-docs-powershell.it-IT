---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: 548e7d19e2d5285ed4063bc9c14202980c02028d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980526"
---
# <span data-ttu-id="a6316-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="a6316-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="a6316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6316-102">SYNOPSIS</span></span>
<span data-ttu-id="a6316-103">Rimuovi le informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="a6316-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="a6316-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6316-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6316-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6316-105">DESCRIPTION</span></span>
<span data-ttu-id="a6316-106">Rimuovi le informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="a6316-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="a6316-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6316-107">EXAMPLES</span></span>

### <span data-ttu-id="a6316-108">Esempio 1: Eliminare un token di registrazione di Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="a6316-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="a6316-109">Questo comando elimina un token di registrazione di Desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="a6316-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="a6316-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6316-110">PARAMETERS</span></span>

### <span data-ttu-id="a6316-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6316-111">-DefaultProfile</span></span>
<span data-ttu-id="a6316-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6316-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6316-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a6316-113">-HostPoolName</span></span>
<span data-ttu-id="a6316-114">Nome pool host</span><span class="sxs-lookup"><span data-stu-id="a6316-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6316-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6316-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6316-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a6316-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6316-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6316-117">-SubscriptionId</span></span>
<span data-ttu-id="a6316-118">aiuto foo 1</span><span class="sxs-lookup"><span data-stu-id="a6316-118">help foo 1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6316-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6316-119">-Confirm</span></span>
<span data-ttu-id="a6316-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6316-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6316-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6316-121">-WhatIf</span></span>
<span data-ttu-id="a6316-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6316-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6316-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6316-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6316-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6316-124">CommonParameters</span></span>
<span data-ttu-id="a6316-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6316-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6316-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6316-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6316-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6316-127">INPUTS</span></span>

## <span data-ttu-id="a6316-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6316-128">OUTPUTS</span></span>

## <span data-ttu-id="a6316-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6316-129">NOTES</span></span>

<span data-ttu-id="a6316-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6316-130">ALIASES</span></span>

## <span data-ttu-id="a6316-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6316-131">RELATED LINKS</span></span>

