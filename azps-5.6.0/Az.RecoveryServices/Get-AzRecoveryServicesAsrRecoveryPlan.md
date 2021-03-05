---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: d3470c3984026232fc90d336e22668868311aa9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963821"
---
# <span data-ttu-id="64f90-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64f90-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="64f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f90-102">SYNOPSIS</span></span>
<span data-ttu-id="64f90-103">Ottiene un piano di ripristino o tutti i piani di ripristino nel vault dei servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="64f90-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="64f90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64f90-104">SYNTAX</span></span>

### <span data-ttu-id="64f90-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64f90-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64f90-106">ByName</span><span class="sxs-lookup"><span data-stu-id="64f90-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64f90-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="64f90-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f90-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64f90-108">DESCRIPTION</span></span>
<span data-ttu-id="64f90-109">Il cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** ottiene i dettagli del piano di ripristino specificato o di tutti i piani di ripristino nel vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="64f90-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="64f90-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64f90-110">EXAMPLES</span></span>

### <span data-ttu-id="64f90-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64f90-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="64f90-112">Ottiene il piano di ripristino con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="64f90-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="64f90-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64f90-113">PARAMETERS</span></span>

### <span data-ttu-id="64f90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f90-114">-DefaultProfile</span></span>
<span data-ttu-id="64f90-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64f90-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="64f90-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="64f90-116">-FriendlyName</span></span>
<span data-ttu-id="64f90-117">Specifica il nome descrittivo del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="64f90-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f90-118">-Name</span><span class="sxs-lookup"><span data-stu-id="64f90-118">-Name</span></span>
<span data-ttu-id="64f90-119">Specifica il nome del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="64f90-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f90-120">-Path</span><span class="sxs-lookup"><span data-stu-id="64f90-120">-Path</span></span>
<span data-ttu-id="64f90-121">Specifica il percorso del file in cui questo cmdlet salva la definizione json del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="64f90-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="64f90-122">La definizione json può essere modificata per modificare il piano di ripristino e usata per aggiornare il piano di ripristino tramite il cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64f90-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f90-123">CommonParameters</span></span>
<span data-ttu-id="64f90-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f90-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64f90-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f90-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="64f90-126">INPUTS</span></span>

### <span data-ttu-id="64f90-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="64f90-127">None</span></span>

## <span data-ttu-id="64f90-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64f90-128">OUTPUTS</span></span>

### <span data-ttu-id="64f90-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64f90-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="64f90-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="64f90-130">NOTES</span></span>

## <span data-ttu-id="64f90-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64f90-131">RELATED LINKS</span></span>

[<span data-ttu-id="64f90-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64f90-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="64f90-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64f90-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="64f90-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64f90-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
