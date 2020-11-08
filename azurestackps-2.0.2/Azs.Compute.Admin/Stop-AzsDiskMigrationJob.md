---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030176"
---
# <span data-ttu-id="1394e-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="1394e-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="1394e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1394e-102">SYNOPSIS</span></span>
<span data-ttu-id="1394e-103">Annullare un processo di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="1394e-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="1394e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1394e-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1394e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1394e-105">DESCRIPTION</span></span>
<span data-ttu-id="1394e-106">Annullare un processo di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="1394e-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="1394e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1394e-107">EXAMPLES</span></span>

### <span data-ttu-id="1394e-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="1394e-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="1394e-109">Annullare un processo di migrazione su disco gestito.</span><span class="sxs-lookup"><span data-stu-id="1394e-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="1394e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1394e-110">PARAMETERS</span></span>

### <span data-ttu-id="1394e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1394e-111">-DefaultProfile</span></span>
<span data-ttu-id="1394e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1394e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1394e-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1394e-113">-Location</span></span>
<span data-ttu-id="1394e-114">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1394e-114">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1394e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1394e-115">-Name</span></span>
<span data-ttu-id="1394e-116">Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="1394e-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1394e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1394e-117">-SubscriptionId</span></span>
<span data-ttu-id="1394e-118">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1394e-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1394e-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1394e-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1394e-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1394e-120">-Confirm</span></span>
<span data-ttu-id="1394e-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1394e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1394e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1394e-122">-WhatIf</span></span>
<span data-ttu-id="1394e-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1394e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1394e-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1394e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1394e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1394e-125">CommonParameters</span></span>
<span data-ttu-id="1394e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1394e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1394e-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1394e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1394e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1394e-128">INPUTS</span></span>

## <span data-ttu-id="1394e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1394e-129">OUTPUTS</span></span>

### <span data-ttu-id="1394e-130">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="1394e-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="1394e-131">Note</span><span class="sxs-lookup"><span data-stu-id="1394e-131">NOTES</span></span>

## <span data-ttu-id="1394e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1394e-132">RELATED LINKS</span></span>

