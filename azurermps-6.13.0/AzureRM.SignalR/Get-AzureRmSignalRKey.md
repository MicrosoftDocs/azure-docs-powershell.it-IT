---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686176"
---
# <span data-ttu-id="58e84-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="58e84-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="58e84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58e84-102">SYNOPSIS</span></span>
<span data-ttu-id="58e84-103">Ottenere i tasti di scelta di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="58e84-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58e84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58e84-104">SYNTAX</span></span>

### <span data-ttu-id="58e84-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58e84-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58e84-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e84-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58e84-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e84-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58e84-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58e84-108">DESCRIPTION</span></span>
<span data-ttu-id="58e84-109">Ottenere i tasti di scelta di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="58e84-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="58e84-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58e84-110">EXAMPLES</span></span>

### <span data-ttu-id="58e84-111">Ottenere i tasti di scelta di un servizio di segnalazione specifico</span><span class="sxs-lookup"><span data-stu-id="58e84-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="58e84-112">Ottenere i tasti di scelta da un oggetto servizio SignalR in pipe</span><span class="sxs-lookup"><span data-stu-id="58e84-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="58e84-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58e84-113">PARAMETERS</span></span>

### <span data-ttu-id="58e84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e84-114">-DefaultProfile</span></span>
<span data-ttu-id="58e84-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58e84-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e84-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58e84-116">-InputObject</span></span>
<span data-ttu-id="58e84-117">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="58e84-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="58e84-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="58e84-118">-Name</span></span>
<span data-ttu-id="58e84-119">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="58e84-119">SignalR service name.</span></span>

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

### <span data-ttu-id="58e84-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e84-120">-ResourceGroupName</span></span>
<span data-ttu-id="58e84-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58e84-121">Resource group name.</span></span>

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

### <span data-ttu-id="58e84-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58e84-122">-ResourceId</span></span>
<span data-ttu-id="58e84-123">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="58e84-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="58e84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e84-124">CommonParameters</span></span>
<span data-ttu-id="58e84-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e84-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e84-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e84-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58e84-127">INPUTS</span></span>

### <span data-ttu-id="58e84-128">System. String</span><span class="sxs-lookup"><span data-stu-id="58e84-128">System.String</span></span>
<span data-ttu-id="58e84-129">Parametri: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58e84-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="58e84-130">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="58e84-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="58e84-131">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58e84-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="58e84-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58e84-132">OUTPUTS</span></span>

### <span data-ttu-id="58e84-133">Microsoft. Azure. Commands. SignalR. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="58e84-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="58e84-134">Note</span><span class="sxs-lookup"><span data-stu-id="58e84-134">NOTES</span></span>

## <span data-ttu-id="58e84-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58e84-135">RELATED LINKS</span></span>
