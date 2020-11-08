---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029937"
---
# <span data-ttu-id="6175f-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6175f-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="6175f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6175f-102">SYNOPSIS</span></span>
<span data-ttu-id="6175f-103">Rimuove una configurazione di bilanciamento del carico interna.</span><span class="sxs-lookup"><span data-stu-id="6175f-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="6175f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6175f-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6175f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6175f-105">DESCRIPTION</span></span>
<span data-ttu-id="6175f-106">Il cmdlet **Remove-AzureInternalLoadBalancer** rimuove la configurazione di bilanciamento del carico interna da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="6175f-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="6175f-107">Se un endpoint fa attualmente riferimento al bilanciamento del carico interno, questo cmdlet non può rimuovere la configurazione.</span><span class="sxs-lookup"><span data-stu-id="6175f-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="6175f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6175f-108">EXAMPLES</span></span>

### <span data-ttu-id="6175f-109">Esempio 1: rimuovere una configurazione di bilanciamento del carico interna</span><span class="sxs-lookup"><span data-stu-id="6175f-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="6175f-110">Questo comando rimuove la configurazione di bilanciamento del carico interna per il servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="6175f-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="6175f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6175f-111">PARAMETERS</span></span>

### <span data-ttu-id="6175f-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6175f-112">-InformationAction</span></span>
<span data-ttu-id="6175f-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6175f-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6175f-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6175f-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6175f-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="6175f-115">Continue</span></span>
- <span data-ttu-id="6175f-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="6175f-116">Ignore</span></span>
- <span data-ttu-id="6175f-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6175f-117">Inquire</span></span>
- <span data-ttu-id="6175f-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6175f-118">SilentlyContinue</span></span>
- <span data-ttu-id="6175f-119">Stop</span><span class="sxs-lookup"><span data-stu-id="6175f-119">Stop</span></span>
- <span data-ttu-id="6175f-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6175f-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6175f-121">-InformationVariable</span></span>
<span data-ttu-id="6175f-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6175f-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="6175f-123">-Profile</span></span>
<span data-ttu-id="6175f-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6175f-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6175f-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6175f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6175f-126">-ServiceName</span></span>
<span data-ttu-id="6175f-127">Specifica il nome del servizio da cui questo cmdlet rimuove un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="6175f-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6175f-128">CommonParameters</span></span>
<span data-ttu-id="6175f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6175f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6175f-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6175f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6175f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6175f-131">INPUTS</span></span>

## <span data-ttu-id="6175f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6175f-132">OUTPUTS</span></span>

### <span data-ttu-id="6175f-133">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="6175f-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="6175f-134">Note</span><span class="sxs-lookup"><span data-stu-id="6175f-134">NOTES</span></span>

## <span data-ttu-id="6175f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6175f-135">RELATED LINKS</span></span>

[<span data-ttu-id="6175f-136">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6175f-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="6175f-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6175f-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="6175f-138">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="6175f-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="6175f-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6175f-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


