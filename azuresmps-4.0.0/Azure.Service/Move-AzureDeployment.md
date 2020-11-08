---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029706"
---
# <span data-ttu-id="d455e-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d455e-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="d455e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d455e-102">SYNOPSIS</span></span>
<span data-ttu-id="d455e-103">Scambia le distribuzioni tra produzione e staging.</span><span class="sxs-lookup"><span data-stu-id="d455e-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="d455e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d455e-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d455e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d455e-105">DESCRIPTION</span></span>
<span data-ttu-id="d455e-106">Il cmdlet **Move-AzureDeployment** scambia gli indirizzi IP virtuali delle distribuzioni in ambienti di produzione e staging.</span><span class="sxs-lookup"><span data-stu-id="d455e-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="d455e-107">Questo cmdlet scambia una distribuzione attualmente eseguita nell'ambiente di gestione temporanea nell'ambiente di produzione e una distribuzione eseguita nell'ambiente di produzione per l'ambiente di staging.</span><span class="sxs-lookup"><span data-stu-id="d455e-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="d455e-108">Se c'è una distribuzione nell'ambiente di staging e nessuna distribuzione nell'ambiente di produzione, il cmdlet sposta la distribuzione in produzione.</span><span class="sxs-lookup"><span data-stu-id="d455e-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="d455e-109">Se è presente una distribuzione nell'ambiente di produzione e nessuna distribuzione nell'ambiente di gestione temporanea, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="d455e-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="d455e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d455e-110">EXAMPLES</span></span>

### <span data-ttu-id="d455e-111">Esempio 1: scambiare distribuzioni per un servizio</span><span class="sxs-lookup"><span data-stu-id="d455e-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="d455e-112">Questo comando scambia le distribuzioni del servizio denominato ContosoService tra gli ambienti di produzione e staging.</span><span class="sxs-lookup"><span data-stu-id="d455e-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="d455e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d455e-113">PARAMETERS</span></span>

### <span data-ttu-id="d455e-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d455e-114">-InformationAction</span></span>
<span data-ttu-id="d455e-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d455e-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d455e-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d455e-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d455e-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="d455e-117">Continue</span></span>
- <span data-ttu-id="d455e-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="d455e-118">Ignore</span></span>
- <span data-ttu-id="d455e-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d455e-119">Inquire</span></span>
- <span data-ttu-id="d455e-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d455e-120">SilentlyContinue</span></span>
- <span data-ttu-id="d455e-121">Stop</span><span class="sxs-lookup"><span data-stu-id="d455e-121">Stop</span></span>
- <span data-ttu-id="d455e-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d455e-122">Suspend</span></span>

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

### <span data-ttu-id="d455e-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d455e-123">-InformationVariable</span></span>
<span data-ttu-id="d455e-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d455e-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d455e-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="d455e-125">-Profile</span></span>
<span data-ttu-id="d455e-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d455e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d455e-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d455e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d455e-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d455e-128">-ServiceName</span></span>
<span data-ttu-id="d455e-129">Specifica il nome del servizio per cui questo cmdlet scambia le distribuzioni di produzione e staging.</span><span class="sxs-lookup"><span data-stu-id="d455e-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="d455e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d455e-130">CommonParameters</span></span>
<span data-ttu-id="d455e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d455e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d455e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d455e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d455e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d455e-133">INPUTS</span></span>

## <span data-ttu-id="d455e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d455e-134">OUTPUTS</span></span>

### <span data-ttu-id="d455e-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="d455e-135">ManagementOperationContext</span></span>

## <span data-ttu-id="d455e-136">Note</span><span class="sxs-lookup"><span data-stu-id="d455e-136">NOTES</span></span>

## <span data-ttu-id="d455e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d455e-137">RELATED LINKS</span></span>

[<span data-ttu-id="d455e-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d455e-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="d455e-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="d455e-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="d455e-140">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d455e-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="d455e-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d455e-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="d455e-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d455e-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


