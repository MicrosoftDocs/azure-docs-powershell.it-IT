---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178607"
---
# <span data-ttu-id="53952-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="53952-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="53952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53952-102">SYNOPSIS</span></span>
<span data-ttu-id="53952-103">Usato per visualizzare il traffico consentito tra le risorse per la sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="53952-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="53952-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53952-104">SYNTAX</span></span>

### <span data-ttu-id="53952-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53952-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53952-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="53952-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53952-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53952-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53952-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="53952-108">DESCRIPTION</span></span>
<span data-ttu-id="53952-109">Ottiene l'elenco di tutto il traffico possibile tra le risorse per la sottoscrizione e la posizione, in base al tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="53952-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="53952-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53952-110">EXAMPLES</span></span>

### <span data-ttu-id="53952-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53952-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="53952-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="53952-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="53952-113">Ottiene l'elenco di tutto il traffico possibile tra le risorse per la sottoscrizione e la posizione, in base al tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="53952-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="53952-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53952-114">PARAMETERS</span></span>

### <span data-ttu-id="53952-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53952-115">-DefaultProfile</span></span>
<span data-ttu-id="53952-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53952-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53952-117">-Location</span><span class="sxs-lookup"><span data-stu-id="53952-117">-Location</span></span>
<span data-ttu-id="53952-118">Posizione.</span><span class="sxs-lookup"><span data-stu-id="53952-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53952-119">-Name</span><span class="sxs-lookup"><span data-stu-id="53952-119">-Name</span></span>
<span data-ttu-id="53952-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="53952-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53952-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53952-121">-ResourceGroupName</span></span>
<span data-ttu-id="53952-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="53952-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53952-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53952-123">-ResourceId</span></span>
<span data-ttu-id="53952-124">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="53952-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53952-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53952-125">CommonParameters</span></span>
<span data-ttu-id="53952-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53952-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53952-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53952-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53952-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="53952-128">INPUTS</span></span>

### <span data-ttu-id="53952-129">System.String</span><span class="sxs-lookup"><span data-stu-id="53952-129">System.String</span></span>

## <span data-ttu-id="53952-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53952-130">OUTPUTS</span></span>

### <span data-ttu-id="53952-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="53952-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="53952-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="53952-132">NOTES</span></span>

## <span data-ttu-id="53952-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53952-133">RELATED LINKS</span></span>
