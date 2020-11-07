---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: acf448b58fdf7bcc218ece8b5fb2415bc30981ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687126"
---
# <span data-ttu-id="59b7c-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="59b7c-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="59b7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="59b7c-103">Avvia un backup per un elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="59b7c-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59b7c-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59b7c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="59b7c-106">Il cmdlet **backup-AzureRmRecoveryServicesBackupItem** avvia un backup per un elemento di backup di Azure protetto che non è legato alla pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="59b7c-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="59b7c-107">È possibile eseguire un backup iniziale subito dopo l'abilitazione della protezione o avviare un backup dopo un errore di backup pianificato.</span><span class="sxs-lookup"><span data-stu-id="59b7c-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="59b7c-108">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="59b7c-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="59b7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59b7c-109">EXAMPLES</span></span>

### <span data-ttu-id="59b7c-110">Esempio 1: avviare un backup per un elemento di backup</span><span class="sxs-lookup"><span data-stu-id="59b7c-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="59b7c-111">Il primo comando ottiene il contenitore di backup di tipo AzureVM denominato pstestv2vm1 e lo archivia nella variabile $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="59b7c-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="59b7c-112">Il secondo comando ottiene l'elemento di backup corrispondente al contenitore in $NamedContainer e lo archivia nella variabile $Item.</span><span class="sxs-lookup"><span data-stu-id="59b7c-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="59b7c-113">L'ultimo comando attiva il processo di backup per l'elemento di backup in $Item.</span><span class="sxs-lookup"><span data-stu-id="59b7c-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="59b7c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59b7c-114">PARAMETERS</span></span>

### <span data-ttu-id="59b7c-115">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="59b7c-115">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="59b7c-116">Specifica un tempo di scadenza come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="59b7c-116">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59b7c-117">-Elemento</span><span class="sxs-lookup"><span data-stu-id="59b7c-117">-Item</span></span>
<span data-ttu-id="59b7c-118">Specifica un elemento di backup per il quale questo cmdlet avvia un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="59b7c-118">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59b7c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b7c-119">-DefaultProfile</span></span>
<span data-ttu-id="59b7c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59b7c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b7c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b7c-121">CommonParameters</span></span>
<span data-ttu-id="59b7c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b7c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b7c-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b7c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b7c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59b7c-124">INPUTS</span></span>

### <span data-ttu-id="59b7c-125">DateTime</span><span class="sxs-lookup"><span data-stu-id="59b7c-125">DateTime</span></span>
<span data-ttu-id="59b7c-126">Il parametro ' ExpiryDateTimeUTC ' accetta il valore di tipo ' DateTime ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="59b7c-126">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="59b7c-127">ItemBase</span><span class="sxs-lookup"><span data-stu-id="59b7c-127">ItemBase</span></span>
<span data-ttu-id="59b7c-128">Il parametro ' Item ' accetta il valore di tipo ' ItemBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="59b7c-128">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="59b7c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59b7c-129">OUTPUTS</span></span>

### <span data-ttu-id="59b7c-130">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="59b7c-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="59b7c-131">Note</span><span class="sxs-lookup"><span data-stu-id="59b7c-131">NOTES</span></span>

## <span data-ttu-id="59b7c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59b7c-132">RELATED LINKS</span></span>

[<span data-ttu-id="59b7c-133">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="59b7c-133">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="59b7c-134">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="59b7c-134">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="59b7c-135">Ripristinare-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="59b7c-135">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


