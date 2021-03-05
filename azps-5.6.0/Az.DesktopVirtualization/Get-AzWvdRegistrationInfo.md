---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 868cbf6aaaf9b9c304c6afa65e63e6eca12910d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962030"
---
# <span data-ttu-id="67f72-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="67f72-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="67f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f72-102">SYNOPSIS</span></span>
<span data-ttu-id="67f72-103">Ottieni le informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="67f72-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="67f72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67f72-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="67f72-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67f72-105">DESCRIPTION</span></span>
<span data-ttu-id="67f72-106">Ottieni le informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="67f72-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="67f72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67f72-107">EXAMPLES</span></span>

### <span data-ttu-id="67f72-108">Esempio 1: Ottenere un token di registrazione di Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="67f72-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="67f72-109">Questo comando ottiene un token di registrazione di Desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="67f72-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="67f72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67f72-110">PARAMETERS</span></span>

### <span data-ttu-id="67f72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f72-111">-DefaultProfile</span></span>
<span data-ttu-id="67f72-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67f72-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f72-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="67f72-113">-HostPoolName</span></span>
<span data-ttu-id="67f72-114">Nome pool host</span><span class="sxs-lookup"><span data-stu-id="67f72-114">Host Pool Name</span></span>

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

### <span data-ttu-id="67f72-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f72-115">-ResourceGroupName</span></span>
<span data-ttu-id="67f72-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="67f72-116">Resource Group Name</span></span>

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

### <span data-ttu-id="67f72-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67f72-117">-SubscriptionId</span></span>
<span data-ttu-id="67f72-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="67f72-118">Subscription Id</span></span>

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

### <span data-ttu-id="67f72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f72-119">CommonParameters</span></span>
<span data-ttu-id="67f72-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f72-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67f72-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f72-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="67f72-122">INPUTS</span></span>

## <span data-ttu-id="67f72-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67f72-123">OUTPUTS</span></span>

### <span data-ttu-id="67f72-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="67f72-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="67f72-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="67f72-125">NOTES</span></span>

<span data-ttu-id="67f72-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="67f72-126">ALIASES</span></span>

## <span data-ttu-id="67f72-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67f72-127">RELATED LINKS</span></span>

