---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 33e0b68e70cb65eee4e9e3178745645aafeb9f9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330904"
---
# <span data-ttu-id="c072d-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c072d-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="c072d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c072d-102">SYNOPSIS</span></span>
<span data-ttu-id="c072d-103">Ottenere le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="c072d-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c072d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c072d-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c072d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c072d-105">DESCRIPTION</span></span>
<span data-ttu-id="c072d-106">Ottenere le informazioni di registrazione di Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="c072d-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c072d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c072d-107">EXAMPLES</span></span>

### <span data-ttu-id="c072d-108">Esempio 1: ottenere un token di registrazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="c072d-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="c072d-109">Questo comando consente di ottenere un token di registrazione desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="c072d-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="c072d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c072d-110">PARAMETERS</span></span>

### <span data-ttu-id="c072d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c072d-111">-DefaultProfile</span></span>
<span data-ttu-id="c072d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c072d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c072d-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c072d-113">-HostPoolName</span></span>
<span data-ttu-id="c072d-114">Nome del pool host</span><span class="sxs-lookup"><span data-stu-id="c072d-114">Host Pool Name</span></span>

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

### <span data-ttu-id="c072d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c072d-115">-ResourceGroupName</span></span>
<span data-ttu-id="c072d-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c072d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c072d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c072d-117">-SubscriptionId</span></span>
<span data-ttu-id="c072d-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="c072d-118">Subscription Id</span></span>

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

### <span data-ttu-id="c072d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c072d-119">CommonParameters</span></span>
<span data-ttu-id="c072d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c072d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c072d-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c072d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c072d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c072d-122">INPUTS</span></span>

## <span data-ttu-id="c072d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c072d-123">OUTPUTS</span></span>

### <span data-ttu-id="c072d-124">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c072d-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.RegistrationInfo</span></span>

## <span data-ttu-id="c072d-125">Note</span><span class="sxs-lookup"><span data-stu-id="c072d-125">NOTES</span></span>

<span data-ttu-id="c072d-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c072d-126">ALIASES</span></span>

## <span data-ttu-id="c072d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c072d-127">RELATED LINKS</span></span>

