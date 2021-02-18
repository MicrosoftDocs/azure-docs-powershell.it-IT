---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 52b2d636e9ab4dbde9cbafc69da3122828a91477
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200503"
---
# <span data-ttu-id="0c027-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="0c027-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="0c027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c027-102">SYNOPSIS</span></span>
<span data-ttu-id="0c027-103">Ottieni le informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c027-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="0c027-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c027-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0c027-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c027-105">DESCRIPTION</span></span>
<span data-ttu-id="0c027-106">Ottieni le informazioni di registrazione del desktop virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c027-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="0c027-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c027-107">EXAMPLES</span></span>

### <span data-ttu-id="0c027-108">Esempio 1: Ottenere un token di registrazione di Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="0c027-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="0c027-109">Questo comando ottiene un token di registrazione di Desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="0c027-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="0c027-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c027-110">PARAMETERS</span></span>

### <span data-ttu-id="0c027-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c027-111">-DefaultProfile</span></span>
<span data-ttu-id="0c027-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c027-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c027-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="0c027-113">-HostPoolName</span></span>
<span data-ttu-id="0c027-114">Nome pool host</span><span class="sxs-lookup"><span data-stu-id="0c027-114">Host Pool Name</span></span>

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

### <span data-ttu-id="0c027-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c027-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c027-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0c027-116">Resource Group Name</span></span>

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

### <span data-ttu-id="0c027-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c027-117">-SubscriptionId</span></span>
<span data-ttu-id="0c027-118">ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="0c027-118">Subscription Id</span></span>

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

### <span data-ttu-id="0c027-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c027-119">CommonParameters</span></span>
<span data-ttu-id="0c027-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c027-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c027-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c027-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c027-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c027-122">INPUTS</span></span>

## <span data-ttu-id="0c027-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c027-123">OUTPUTS</span></span>

### <span data-ttu-id="0c027-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="0c027-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="0c027-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c027-125">NOTES</span></span>

<span data-ttu-id="0c027-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0c027-126">ALIASES</span></span>

## <span data-ttu-id="0c027-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c027-127">RELATED LINKS</span></span>

