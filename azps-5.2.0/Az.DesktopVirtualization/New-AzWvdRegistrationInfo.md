---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 2268135ebd1e1c504aae7462730d104e842f288f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332611"
---
# <span data-ttu-id="6cc34-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="6cc34-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="6cc34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cc34-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc34-103">Creare le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="6cc34-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="6cc34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cc34-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cc34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cc34-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc34-106">Creare le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="6cc34-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="6cc34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cc34-107">EXAMPLES</span></span>

### <span data-ttu-id="6cc34-108">Esempio 1: creare un token di registrazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="6cc34-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="6cc34-109">Questo comando crea un token di registrazione desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="6cc34-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="6cc34-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cc34-110">PARAMETERS</span></span>

### <span data-ttu-id="6cc34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc34-111">-DefaultProfile</span></span>
<span data-ttu-id="6cc34-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc34-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc34-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="6cc34-113">-ExpirationTime</span></span>
<span data-ttu-id="6cc34-114">Data di scadenza</span><span class="sxs-lookup"><span data-stu-id="6cc34-114">Expiration Time</span></span>

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

### <span data-ttu-id="6cc34-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6cc34-115">-HostPoolName</span></span>
<span data-ttu-id="6cc34-116">Nome del pool host</span><span class="sxs-lookup"><span data-stu-id="6cc34-116">Host Pool Name</span></span>

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

### <span data-ttu-id="6cc34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc34-117">-ResourceGroupName</span></span>
<span data-ttu-id="6cc34-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6cc34-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6cc34-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cc34-119">-SubscriptionId</span></span>
<span data-ttu-id="6cc34-120">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="6cc34-120">Subscription Id</span></span>

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

### <span data-ttu-id="6cc34-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6cc34-121">-Confirm</span></span>
<span data-ttu-id="6cc34-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cc34-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc34-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc34-123">-WhatIf</span></span>
<span data-ttu-id="6cc34-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cc34-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc34-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cc34-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc34-126">CommonParameters</span></span>
<span data-ttu-id="6cc34-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc34-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cc34-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc34-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cc34-129">INPUTS</span></span>

## <span data-ttu-id="6cc34-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cc34-130">OUTPUTS</span></span>

### <span data-ttu-id="6cc34-131">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="6cc34-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="6cc34-132">Note</span><span class="sxs-lookup"><span data-stu-id="6cc34-132">NOTES</span></span>

<span data-ttu-id="6cc34-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6cc34-133">ALIASES</span></span>

## <span data-ttu-id="6cc34-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cc34-134">RELATED LINKS</span></span>

