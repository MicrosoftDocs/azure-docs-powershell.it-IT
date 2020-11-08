---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190218"
---
# <span data-ttu-id="d67a5-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="d67a5-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="d67a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d67a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d67a5-103">Rimuovere le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="d67a5-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d67a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d67a5-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d67a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d67a5-105">DESCRIPTION</span></span>
<span data-ttu-id="d67a5-106">Rimuovere le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="d67a5-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d67a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d67a5-107">EXAMPLES</span></span>

### <span data-ttu-id="d67a5-108">Esempio 1: eliminare un token di registrazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="d67a5-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="d67a5-109">Questo comando Elimina un token di registrazione desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="d67a5-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="d67a5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d67a5-110">PARAMETERS</span></span>

### <span data-ttu-id="d67a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67a5-111">-DefaultProfile</span></span>
<span data-ttu-id="d67a5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d67a5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d67a5-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d67a5-113">-HostPoolName</span></span>
<span data-ttu-id="d67a5-114">Nome del pool host</span><span class="sxs-lookup"><span data-stu-id="d67a5-114">Host Pool Name</span></span>

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

### <span data-ttu-id="d67a5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67a5-115">-ResourceGroupName</span></span>
<span data-ttu-id="d67a5-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d67a5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d67a5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d67a5-117">-SubscriptionId</span></span>
<span data-ttu-id="d67a5-118">Guida di pippo 1</span><span class="sxs-lookup"><span data-stu-id="d67a5-118">help foo 1</span></span>

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

### <span data-ttu-id="d67a5-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d67a5-119">-Confirm</span></span>
<span data-ttu-id="d67a5-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d67a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d67a5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d67a5-121">-WhatIf</span></span>
<span data-ttu-id="d67a5-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d67a5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d67a5-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d67a5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d67a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67a5-124">CommonParameters</span></span>
<span data-ttu-id="d67a5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67a5-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d67a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67a5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d67a5-127">INPUTS</span></span>

## <span data-ttu-id="d67a5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d67a5-128">OUTPUTS</span></span>

## <span data-ttu-id="d67a5-129">Note</span><span class="sxs-lookup"><span data-stu-id="d67a5-129">NOTES</span></span>

<span data-ttu-id="d67a5-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d67a5-130">ALIASES</span></span>

## <span data-ttu-id="d67a5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d67a5-131">RELATED LINKS</span></span>

