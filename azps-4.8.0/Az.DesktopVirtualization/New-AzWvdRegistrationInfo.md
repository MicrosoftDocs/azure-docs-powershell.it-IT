---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192972"
---
# <span data-ttu-id="99361-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="99361-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="99361-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99361-102">SYNOPSIS</span></span>
<span data-ttu-id="99361-103">Creare le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="99361-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="99361-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99361-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99361-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99361-105">DESCRIPTION</span></span>
<span data-ttu-id="99361-106">Creare le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="99361-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="99361-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99361-107">EXAMPLES</span></span>

### <span data-ttu-id="99361-108">Esempio 1: creare un token di registrazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="99361-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="99361-109">Questo comando crea un token di registrazione desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="99361-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="99361-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99361-110">PARAMETERS</span></span>

### <span data-ttu-id="99361-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99361-111">-DefaultProfile</span></span>
<span data-ttu-id="99361-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99361-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99361-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="99361-113">-ExpirationTime</span></span>
<span data-ttu-id="99361-114">Data di scadenza</span><span class="sxs-lookup"><span data-stu-id="99361-114">Expiration Time</span></span>

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

### <span data-ttu-id="99361-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="99361-115">-HostPoolName</span></span>
<span data-ttu-id="99361-116">Nome del pool host</span><span class="sxs-lookup"><span data-stu-id="99361-116">Host Pool Name</span></span>

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

### <span data-ttu-id="99361-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99361-117">-ResourceGroupName</span></span>
<span data-ttu-id="99361-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="99361-118">Resource Group Name</span></span>

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

### <span data-ttu-id="99361-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99361-119">-SubscriptionId</span></span>
<span data-ttu-id="99361-120">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="99361-120">Subscription Id</span></span>

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

### <span data-ttu-id="99361-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99361-121">-Confirm</span></span>
<span data-ttu-id="99361-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99361-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99361-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99361-123">-WhatIf</span></span>
<span data-ttu-id="99361-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99361-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99361-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99361-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99361-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99361-126">CommonParameters</span></span>
<span data-ttu-id="99361-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99361-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99361-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99361-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99361-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99361-129">INPUTS</span></span>

## <span data-ttu-id="99361-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99361-130">OUTPUTS</span></span>

### <span data-ttu-id="99361-131">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="99361-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="99361-132">Note</span><span class="sxs-lookup"><span data-stu-id="99361-132">NOTES</span></span>

<span data-ttu-id="99361-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="99361-133">ALIASES</span></span>

## <span data-ttu-id="99361-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99361-134">RELATED LINKS</span></span>

