---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031780"
---
# <span data-ttu-id="7cef8-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="7cef8-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="7cef8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cef8-102">SYNOPSIS</span></span>
<span data-ttu-id="7cef8-103">Ottenere le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="7cef8-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="7cef8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cef8-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7cef8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cef8-105">DESCRIPTION</span></span>
<span data-ttu-id="7cef8-106">Ottenere le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="7cef8-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="7cef8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cef8-107">EXAMPLES</span></span>

### <span data-ttu-id="7cef8-108">Esempio 1: ottenere un token di registrazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="7cef8-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="7cef8-109">Questo comando consente di ottenere un token di registrazione desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="7cef8-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="7cef8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cef8-110">PARAMETERS</span></span>

### <span data-ttu-id="7cef8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cef8-111">-DefaultProfile</span></span>
<span data-ttu-id="7cef8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cef8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cef8-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="7cef8-113">-HostPoolName</span></span>
<span data-ttu-id="7cef8-114">Nome del pool host</span><span class="sxs-lookup"><span data-stu-id="7cef8-114">Host Pool Name</span></span>

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

### <span data-ttu-id="7cef8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cef8-115">-ResourceGroupName</span></span>
<span data-ttu-id="7cef8-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7cef8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="7cef8-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cef8-117">-SubscriptionId</span></span>
<span data-ttu-id="7cef8-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="7cef8-118">Subscription Id</span></span>

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

### <span data-ttu-id="7cef8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cef8-119">CommonParameters</span></span>
<span data-ttu-id="7cef8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cef8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cef8-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cef8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cef8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cef8-122">INPUTS</span></span>

## <span data-ttu-id="7cef8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cef8-123">OUTPUTS</span></span>

### <span data-ttu-id="7cef8-124">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="7cef8-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="7cef8-125">Note</span><span class="sxs-lookup"><span data-stu-id="7cef8-125">NOTES</span></span>

<span data-ttu-id="7cef8-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7cef8-126">ALIASES</span></span>

## <span data-ttu-id="7cef8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cef8-127">RELATED LINKS</span></span>

