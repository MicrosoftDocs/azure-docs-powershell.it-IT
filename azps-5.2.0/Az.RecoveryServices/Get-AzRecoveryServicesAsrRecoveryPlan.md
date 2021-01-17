---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352636"
---
# <span data-ttu-id="6b42c-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b42c-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6b42c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b42c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b42c-103">Ottiene un piano di ripristino o tutti i piani di ripristino nel Vault di servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="6b42c-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="6b42c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b42c-104">SYNTAX</span></span>

### <span data-ttu-id="6b42c-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b42c-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b42c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6b42c-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b42c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b42c-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b42c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b42c-108">DESCRIPTION</span></span>
<span data-ttu-id="6b42c-109">Il cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** consente di ottenere i dettagli del piano di ripristino specificato o di tutti i piani di ripristino nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6b42c-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="6b42c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b42c-110">EXAMPLES</span></span>

### <span data-ttu-id="6b42c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b42c-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="6b42c-112">Ottiene il piano di ripristino con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6b42c-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="6b42c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b42c-113">PARAMETERS</span></span>

### <span data-ttu-id="6b42c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b42c-114">-DefaultProfile</span></span>
<span data-ttu-id="6b42c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b42c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b42c-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b42c-116">-FriendlyName</span></span>
<span data-ttu-id="6b42c-117">Specifica il nome descrittivo del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6b42c-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="6b42c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b42c-118">-Name</span></span>
<span data-ttu-id="6b42c-119">Specifica il nome del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6b42c-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="6b42c-120">-Path</span><span class="sxs-lookup"><span data-stu-id="6b42c-120">-Path</span></span>
<span data-ttu-id="6b42c-121">Specifica il percorso del file a cui questo cmdlet salva la definizione JSON del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6b42c-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="6b42c-122">La definizione JSON può essere modificata per modificare il piano di ripristino e usato per aggiornare il piano di ripristino tramite il cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b42c-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="6b42c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b42c-123">CommonParameters</span></span>
<span data-ttu-id="6b42c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b42c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b42c-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b42c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b42c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b42c-126">INPUTS</span></span>

### <span data-ttu-id="6b42c-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6b42c-127">None</span></span>

## <span data-ttu-id="6b42c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b42c-128">OUTPUTS</span></span>

### <span data-ttu-id="6b42c-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b42c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="6b42c-130">Note</span><span class="sxs-lookup"><span data-stu-id="6b42c-130">NOTES</span></span>

## <span data-ttu-id="6b42c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b42c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b42c-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b42c-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6b42c-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b42c-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6b42c-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b42c-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
