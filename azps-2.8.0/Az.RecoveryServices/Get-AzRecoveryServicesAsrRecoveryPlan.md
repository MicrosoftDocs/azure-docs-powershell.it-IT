---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 8c4bc3598d18042d31e98b37d9fc2c09d45b74d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855786"
---
# <span data-ttu-id="3f82e-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f82e-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="3f82e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f82e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f82e-103">Ottiene un piano di ripristino o tutti i piani di ripristino nel Vault di servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="3f82e-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="3f82e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f82e-104">SYNTAX</span></span>

### <span data-ttu-id="3f82e-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f82e-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f82e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3f82e-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f82e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f82e-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f82e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f82e-108">DESCRIPTION</span></span>
<span data-ttu-id="3f82e-109">Il cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** consente di ottenere i dettagli del piano di ripristino specificato o di tutti i piani di ripristino nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3f82e-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="3f82e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f82e-110">EXAMPLES</span></span>

### <span data-ttu-id="3f82e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f82e-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="3f82e-112">Ottiene il piano di ripristino con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="3f82e-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="3f82e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f82e-113">PARAMETERS</span></span>

### <span data-ttu-id="3f82e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f82e-114">-DefaultProfile</span></span>
<span data-ttu-id="3f82e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f82e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3f82e-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f82e-116">-FriendlyName</span></span>
<span data-ttu-id="3f82e-117">Specifica il nome descrittivo del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3f82e-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="3f82e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f82e-118">-Name</span></span>
<span data-ttu-id="3f82e-119">Specifica il nome del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3f82e-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="3f82e-120">-Path</span><span class="sxs-lookup"><span data-stu-id="3f82e-120">-Path</span></span>
<span data-ttu-id="3f82e-121">Specifica il percorso del file a cui questo cmdlet salva la definizione JSON del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3f82e-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="3f82e-122">La definizione JSON può essere modificata per modificare il piano di ripristino e usato per aggiornare il piano di ripristino tramite il cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f82e-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="3f82e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f82e-123">CommonParameters</span></span>
<span data-ttu-id="3f82e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f82e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f82e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f82e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f82e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f82e-126">INPUTS</span></span>

### <span data-ttu-id="3f82e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3f82e-127">None</span></span>

## <span data-ttu-id="3f82e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f82e-128">OUTPUTS</span></span>

### <span data-ttu-id="3f82e-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f82e-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="3f82e-130">Note</span><span class="sxs-lookup"><span data-stu-id="3f82e-130">NOTES</span></span>

## <span data-ttu-id="3f82e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f82e-131">RELATED LINKS</span></span>

[<span data-ttu-id="3f82e-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f82e-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="3f82e-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f82e-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="3f82e-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f82e-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
