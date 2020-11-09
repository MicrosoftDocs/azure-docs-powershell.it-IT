---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302424"
---
# <span data-ttu-id="16c27-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="16c27-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="16c27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16c27-102">SYNOPSIS</span></span>
<span data-ttu-id="16c27-103">Ottenere i tasti di scelta di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="16c27-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="16c27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16c27-104">SYNTAX</span></span>

### <span data-ttu-id="16c27-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16c27-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16c27-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16c27-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c27-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16c27-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c27-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16c27-108">DESCRIPTION</span></span>
<span data-ttu-id="16c27-109">Ottenere i tasti di scelta di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="16c27-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="16c27-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16c27-110">EXAMPLES</span></span>

### <span data-ttu-id="16c27-111">Ottenere i tasti di scelta di un servizio di segnalazione specifico</span><span class="sxs-lookup"><span data-stu-id="16c27-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="16c27-112">Ottenere i tasti di scelta da un oggetto servizio SignalR in pipe</span><span class="sxs-lookup"><span data-stu-id="16c27-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="16c27-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16c27-113">PARAMETERS</span></span>

### <span data-ttu-id="16c27-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c27-114">-DefaultProfile</span></span>
<span data-ttu-id="16c27-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16c27-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c27-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16c27-116">-InputObject</span></span>
<span data-ttu-id="16c27-117">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="16c27-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="16c27-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="16c27-118">-Name</span></span>
<span data-ttu-id="16c27-119">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="16c27-119">SignalR service name.</span></span>

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

### <span data-ttu-id="16c27-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c27-120">-ResourceGroupName</span></span>
<span data-ttu-id="16c27-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16c27-121">Resource group name.</span></span>

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

### <span data-ttu-id="16c27-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16c27-122">-ResourceId</span></span>
<span data-ttu-id="16c27-123">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="16c27-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="16c27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c27-124">CommonParameters</span></span>
<span data-ttu-id="16c27-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c27-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16c27-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c27-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16c27-127">INPUTS</span></span>

### <span data-ttu-id="16c27-128">System. String</span><span class="sxs-lookup"><span data-stu-id="16c27-128">System.String</span></span>
### <span data-ttu-id="16c27-129">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="16c27-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="16c27-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16c27-130">OUTPUTS</span></span>

### <span data-ttu-id="16c27-131">Microsoft. Azure. Commands. SignalR. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="16c27-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="16c27-132">Note</span><span class="sxs-lookup"><span data-stu-id="16c27-132">NOTES</span></span>

## <span data-ttu-id="16c27-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16c27-133">RELATED LINKS</span></span>
