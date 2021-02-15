---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189039"
---
# <span data-ttu-id="21c4f-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="21c4f-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="21c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="21c4f-103">Ottieni i tasti di scelta di un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="21c4f-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="21c4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21c4f-104">SYNTAX</span></span>

### <span data-ttu-id="21c4f-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21c4f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21c4f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c4f-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c4f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c4f-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21c4f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21c4f-108">DESCRIPTION</span></span>
<span data-ttu-id="21c4f-109">Ottieni i tasti di scelta di un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="21c4f-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="21c4f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21c4f-110">EXAMPLES</span></span>

### <span data-ttu-id="21c4f-111">Ottieni i tasti di scelta di uno specifico servizio SignalR</span><span class="sxs-lookup"><span data-stu-id="21c4f-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="21c4f-112">Ottenere i tasti di scelta da un oggetto servizio SignalR in pipe</span><span class="sxs-lookup"><span data-stu-id="21c4f-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="21c4f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21c4f-113">PARAMETERS</span></span>

### <span data-ttu-id="21c4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c4f-114">-DefaultProfile</span></span>
<span data-ttu-id="21c4f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21c4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c4f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21c4f-116">-InputObject</span></span>
<span data-ttu-id="21c4f-117">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="21c4f-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21c4f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="21c4f-118">-Name</span></span>
<span data-ttu-id="21c4f-119">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="21c4f-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c4f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c4f-120">-ResourceGroupName</span></span>
<span data-ttu-id="21c4f-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21c4f-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c4f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21c4f-122">-ResourceId</span></span>
<span data-ttu-id="21c4f-123">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="21c4f-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21c4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c4f-124">CommonParameters</span></span>
<span data-ttu-id="21c4f-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c4f-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21c4f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c4f-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="21c4f-127">INPUTS</span></span>

### <span data-ttu-id="21c4f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="21c4f-128">System.String</span></span>
### <span data-ttu-id="21c4f-129">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="21c4f-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="21c4f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21c4f-130">OUTPUTS</span></span>

### <span data-ttu-id="21c4f-131">Microsoft.Azure.Commands.Signalr.Models.PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="21c4f-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="21c4f-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="21c4f-132">NOTES</span></span>

## <span data-ttu-id="21c4f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21c4f-133">RELATED LINKS</span></span>
