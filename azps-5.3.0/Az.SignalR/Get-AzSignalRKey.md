---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474937"
---
# <span data-ttu-id="b1881-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="b1881-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="b1881-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1881-102">SYNOPSIS</span></span>
<span data-ttu-id="b1881-103">Ottenere i tasti di scelta di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="b1881-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="b1881-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1881-104">SYNTAX</span></span>

### <span data-ttu-id="b1881-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1881-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1881-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1881-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1881-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1881-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1881-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1881-108">DESCRIPTION</span></span>
<span data-ttu-id="b1881-109">Ottenere i tasti di scelta di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="b1881-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="b1881-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1881-110">EXAMPLES</span></span>

### <span data-ttu-id="b1881-111">Ottenere i tasti di scelta di un servizio di segnalazione specifico</span><span class="sxs-lookup"><span data-stu-id="b1881-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="b1881-112">Ottenere i tasti di scelta da un oggetto servizio SignalR in pipe</span><span class="sxs-lookup"><span data-stu-id="b1881-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="b1881-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1881-113">PARAMETERS</span></span>

### <span data-ttu-id="b1881-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1881-114">-DefaultProfile</span></span>
<span data-ttu-id="b1881-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1881-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1881-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1881-116">-InputObject</span></span>
<span data-ttu-id="b1881-117">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="b1881-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b1881-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1881-118">-Name</span></span>
<span data-ttu-id="b1881-119">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="b1881-119">SignalR service name.</span></span>

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

### <span data-ttu-id="b1881-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1881-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1881-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1881-121">Resource group name.</span></span>

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

### <span data-ttu-id="b1881-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1881-122">-ResourceId</span></span>
<span data-ttu-id="b1881-123">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="b1881-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="b1881-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1881-124">CommonParameters</span></span>
<span data-ttu-id="b1881-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1881-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1881-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1881-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1881-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1881-127">INPUTS</span></span>

### <span data-ttu-id="b1881-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b1881-128">System.String</span></span>
### <span data-ttu-id="b1881-129">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b1881-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="b1881-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1881-130">OUTPUTS</span></span>

### <span data-ttu-id="b1881-131">Microsoft. Azure. Commands. SignalR. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="b1881-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="b1881-132">Note</span><span class="sxs-lookup"><span data-stu-id="b1881-132">NOTES</span></span>

## <span data-ttu-id="b1881-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1881-133">RELATED LINKS</span></span>
