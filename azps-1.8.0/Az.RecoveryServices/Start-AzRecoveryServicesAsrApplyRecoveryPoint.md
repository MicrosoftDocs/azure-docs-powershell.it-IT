---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2e67ccc4fa97cc6cc5c9a212055118bbd14db785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399738"
---
# <span data-ttu-id="a07d8-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a07d8-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="a07d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07d8-102">SYNOPSIS</span></span>
<span data-ttu-id="a07d8-103">Modifica un punto di ripristino per un elemento protetto con failover prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="a07d8-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

## <span data-ttu-id="a07d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a07d8-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a07d8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a07d8-105">DESCRIPTION</span></span>
<span data-ttu-id="a07d8-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** cambia il punto di ripristino per un elemento protetto con failover prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="a07d8-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="a07d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a07d8-107">EXAMPLES</span></span>

### <span data-ttu-id="a07d8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a07d8-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="a07d8-109">Avvia l'applicazione del punto di ripristino specificato all'elemento protetto da replica e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a07d8-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a07d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a07d8-110">PARAMETERS</span></span>

### <span data-ttu-id="a07d8-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a07d8-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="a07d8-112">Specifica il file del certificato primario se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="a07d8-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07d8-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a07d8-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="a07d8-114">Specifica il file del certificato secondario se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="a07d8-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07d8-115">-DefaultProfile</span></span>
<span data-ttu-id="a07d8-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a07d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a07d8-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a07d8-117">-RecoveryPoint</span></span>
<span data-ttu-id="a07d8-118">Specifica l'oggetto punto di ripristino corrispondente al punto di ripristino da applicare.</span><span class="sxs-lookup"><span data-stu-id="a07d8-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07d8-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a07d8-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a07d8-120">Specifica l'oggetto elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="a07d8-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a07d8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a07d8-121">-Confirm</span></span>
<span data-ttu-id="a07d8-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a07d8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a07d8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07d8-123">-WhatIf</span></span>
<span data-ttu-id="a07d8-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a07d8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a07d8-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a07d8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a07d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07d8-126">CommonParameters</span></span>
<span data-ttu-id="a07d8-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07d8-128">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07d8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07d8-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="a07d8-129">INPUTS</span></span>

### <span data-ttu-id="a07d8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a07d8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a07d8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a07d8-131">OUTPUTS</span></span>

### <span data-ttu-id="a07d8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a07d8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a07d8-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="a07d8-133">NOTES</span></span>

## <span data-ttu-id="a07d8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a07d8-134">RELATED LINKS</span></span>


