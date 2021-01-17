---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477911"
---
# <span data-ttu-id="c001d-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="c001d-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="c001d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c001d-102">SYNOPSIS</span></span>
<span data-ttu-id="c001d-103">Ottenere i tasti di scelta della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c001d-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="c001d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c001d-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c001d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c001d-105">DESCRIPTION</span></span>
<span data-ttu-id="c001d-106">Ottenere i tasti di scelta della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c001d-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="c001d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c001d-107">EXAMPLES</span></span>

### <span data-ttu-id="c001d-108">Esempio 1: recuperare la chiave per il servizio communcation specificato</span><span class="sxs-lookup"><span data-stu-id="c001d-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="c001d-109">Visualizza la ConnectionString e la chiave per il servizio communcation specificato.</span><span class="sxs-lookup"><span data-stu-id="c001d-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="c001d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c001d-110">PARAMETERS</span></span>

### <span data-ttu-id="c001d-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="c001d-111">-CommunicationServiceName</span></span>
<span data-ttu-id="c001d-112">Il nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c001d-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="c001d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c001d-113">-DefaultProfile</span></span>
<span data-ttu-id="c001d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c001d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c001d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c001d-115">-ResourceGroupName</span></span>
<span data-ttu-id="c001d-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c001d-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c001d-117">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c001d-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c001d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c001d-118">-SubscriptionId</span></span>
<span data-ttu-id="c001d-119">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c001d-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c001d-120">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c001d-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c001d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c001d-121">-Confirm</span></span>
<span data-ttu-id="c001d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c001d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c001d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c001d-123">-WhatIf</span></span>
<span data-ttu-id="c001d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c001d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c001d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c001d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c001d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c001d-126">CommonParameters</span></span>
<span data-ttu-id="c001d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c001d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c001d-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c001d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c001d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c001d-129">INPUTS</span></span>

## <span data-ttu-id="c001d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c001d-130">OUTPUTS</span></span>

### <span data-ttu-id="c001d-131">Microsoft. Azure. PowerShell. Cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="c001d-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="c001d-132">Note</span><span class="sxs-lookup"><span data-stu-id="c001d-132">NOTES</span></span>

<span data-ttu-id="c001d-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c001d-133">ALIASES</span></span>

## <span data-ttu-id="c001d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c001d-134">RELATED LINKS</span></span>

