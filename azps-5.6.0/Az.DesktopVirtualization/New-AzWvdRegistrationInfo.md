---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 7e633d2ba607132de6dbdfc262642659cc5e4c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966109"
---
# <span data-ttu-id="976fc-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="976fc-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="976fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="976fc-102">SYNOPSIS</span></span>
<span data-ttu-id="976fc-103">Crea informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="976fc-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="976fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="976fc-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="976fc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="976fc-105">DESCRIPTION</span></span>
<span data-ttu-id="976fc-106">Crea informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="976fc-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="976fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="976fc-107">EXAMPLES</span></span>

### <span data-ttu-id="976fc-108">Esempio 1: Creare un token di registrazione di Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="976fc-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="976fc-109">Questo comando crea un token di registrazione di Desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="976fc-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="976fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="976fc-110">PARAMETERS</span></span>

### <span data-ttu-id="976fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976fc-111">-DefaultProfile</span></span>
<span data-ttu-id="976fc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="976fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="976fc-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="976fc-113">-ExpirationTime</span></span>
<span data-ttu-id="976fc-114">Ora scadenza</span><span class="sxs-lookup"><span data-stu-id="976fc-114">Expiration Time</span></span>

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

### <span data-ttu-id="976fc-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="976fc-115">-HostPoolName</span></span>
<span data-ttu-id="976fc-116">Nome pool host</span><span class="sxs-lookup"><span data-stu-id="976fc-116">Host Pool Name</span></span>

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

### <span data-ttu-id="976fc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976fc-117">-ResourceGroupName</span></span>
<span data-ttu-id="976fc-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="976fc-118">Resource Group Name</span></span>

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

### <span data-ttu-id="976fc-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="976fc-119">-SubscriptionId</span></span>
<span data-ttu-id="976fc-120">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="976fc-120">Subscription Id</span></span>

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

### <span data-ttu-id="976fc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="976fc-121">-Confirm</span></span>
<span data-ttu-id="976fc-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="976fc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="976fc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976fc-123">-WhatIf</span></span>
<span data-ttu-id="976fc-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="976fc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="976fc-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="976fc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="976fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976fc-126">CommonParameters</span></span>
<span data-ttu-id="976fc-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976fc-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="976fc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976fc-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="976fc-129">INPUTS</span></span>

## <span data-ttu-id="976fc-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="976fc-130">OUTPUTS</span></span>

### <span data-ttu-id="976fc-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="976fc-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="976fc-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="976fc-132">NOTES</span></span>

<span data-ttu-id="976fc-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="976fc-133">ALIASES</span></span>

## <span data-ttu-id="976fc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="976fc-134">RELATED LINKS</span></span>

