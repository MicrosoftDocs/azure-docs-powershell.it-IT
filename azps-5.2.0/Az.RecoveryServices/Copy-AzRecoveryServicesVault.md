---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341584"
---
# <span data-ttu-id="8fced-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8fced-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="8fced-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fced-102">SYNOPSIS</span></span>
<span data-ttu-id="8fced-103">Copia i dati da un Vault in un'area geografica in un caveau di un'altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="8fced-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="8fced-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fced-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="8fced-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fced-105">DESCRIPTION</span></span>
<span data-ttu-id="8fced-106">Il cmdlet **Copy-AzRecoveryServicesVault** copia i dati da un Vault in un'area geografica in un Vault in un'altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="8fced-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="8fced-107">Attualmente è supportata solo la migrazione dei dati a livello di volta.</span><span class="sxs-lookup"><span data-stu-id="8fced-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="8fced-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fced-108">EXAMPLES</span></span>

### <span data-ttu-id="8fced-109">Esempio 1: copiare i dati da vault1 a vault2</span><span class="sxs-lookup"><span data-stu-id="8fced-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="8fced-110">I primi due cmdlet recuperano rispettivamente i servizi di recupero di vault1 e vault2.</span><span class="sxs-lookup"><span data-stu-id="8fced-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="8fced-111">Il secondo comando attiva un trasferimento completo di dati da vault1 a vault2.</span><span class="sxs-lookup"><span data-stu-id="8fced-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="8fced-112">Esempio 2: copiare i dati da vault1 a vault2 con solo gli elementi non riusciti</span><span class="sxs-lookup"><span data-stu-id="8fced-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

<span data-ttu-id="8fced-113">I primi due cmdlet recuperano rispettivamente i servizi di recupero di vault1 e vault2.</span><span class="sxs-lookup"><span data-stu-id="8fced-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="8fced-114">Il secondo comando attiva un trasferimento parziale di dati da vault1 a vault2 con solo gli elementi che non sono riusciti nelle operazioni di movimento precedenti.</span><span class="sxs-lookup"><span data-stu-id="8fced-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="8fced-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fced-115">PARAMETERS</span></span>

### <span data-ttu-id="8fced-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fced-116">-DefaultProfile</span></span>
<span data-ttu-id="8fced-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fced-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fced-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8fced-118">-Force</span></span>
<span data-ttu-id="8fced-119">Impone l'operazione di trasferimento dati (impedisce la finestra di dialogo di conferma) senza chiedere conferma per il tipo di ridondanza dello spazio di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8fced-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="8fced-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8fced-120">This parameter is optional.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fced-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="8fced-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="8fced-122">Parametro switch per provare lo spostamento dei dati solo per i contenitori nel caveau di origine che non sono ancora stati spostati.</span><span class="sxs-lookup"><span data-stu-id="8fced-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fced-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="8fced-123">-SourceVault</span></span>
<span data-ttu-id="8fced-124">Oggetto del Vault di origine da spostare.</span><span class="sxs-lookup"><span data-stu-id="8fced-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fced-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="8fced-125">-TargetVault</span></span>
<span data-ttu-id="8fced-126">Oggetto Vault di destinazione in cui devono essere spostati i dati.</span><span class="sxs-lookup"><span data-stu-id="8fced-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fced-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fced-127">CommonParameters</span></span>
<span data-ttu-id="8fced-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fced-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fced-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fced-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fced-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fced-130">INPUTS</span></span>

### <span data-ttu-id="8fced-131">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="8fced-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="8fced-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fced-132">OUTPUTS</span></span>

### <span data-ttu-id="8fced-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8fced-133">System.String</span></span>

## <span data-ttu-id="8fced-134">Note</span><span class="sxs-lookup"><span data-stu-id="8fced-134">NOTES</span></span>

## <span data-ttu-id="8fced-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fced-135">RELATED LINKS</span></span>
