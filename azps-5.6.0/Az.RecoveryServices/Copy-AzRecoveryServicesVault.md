---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960254"
---
# <span data-ttu-id="fc488-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="fc488-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="fc488-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc488-102">SYNOPSIS</span></span>
<span data-ttu-id="fc488-103">Copia i dati da un vault di un'area a un vault in un'altra area.</span><span class="sxs-lookup"><span data-stu-id="fc488-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="fc488-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc488-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="fc488-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc488-105">DESCRIPTION</span></span>
<span data-ttu-id="fc488-106">Il cmdlet **Copy-AzRecoveryServicesVault** copia i dati da un vault di un'area geografica a un vault in un'altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="fc488-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="fc488-107">Attualmente è supportati solo lo spostamento dei dati a livello di vault.</span><span class="sxs-lookup"><span data-stu-id="fc488-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="fc488-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc488-108">EXAMPLES</span></span>

### <span data-ttu-id="fc488-109">Esempio 1: Copiare i dati da vault1 a vault2</span><span class="sxs-lookup"><span data-stu-id="fc488-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="fc488-110">I primi due cmdlet recuperano rispettivamente vault dei servizi di recupero, vault1 e vault2.</span><span class="sxs-lookup"><span data-stu-id="fc488-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="fc488-111">Il secondo comando attiva uno spostamento completo di dati da vault1 a vault2.</span><span class="sxs-lookup"><span data-stu-id="fc488-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="fc488-112">Esempio 2: Copiare i dati da vault1 a vault2 con solo elementi non riusciti</span><span class="sxs-lookup"><span data-stu-id="fc488-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="fc488-113">I primi due cmdlet recuperano rispettivamente vault dei servizi di recupero, vault1 e vault2.</span><span class="sxs-lookup"><span data-stu-id="fc488-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="fc488-114">Il secondo comando attiva uno spostamento parziale di dati da vault1 a vault2 con solo gli elementi non riusciti nelle operazioni di spostamento precedenti.</span><span class="sxs-lookup"><span data-stu-id="fc488-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="fc488-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc488-115">PARAMETERS</span></span>

### <span data-ttu-id="fc488-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc488-116">-DefaultProfile</span></span>
<span data-ttu-id="fc488-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc488-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc488-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fc488-118">-Force</span></span>
<span data-ttu-id="fc488-119">Forza l'operazione di spostamento dei dati (impedisce la finestra di dialogo di conferma) senza chiedere conferma per il tipo di ridondanza di archiviazione del vault di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fc488-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="fc488-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc488-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="fc488-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="fc488-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="fc488-122">Passare al parametro per provare lo spostamento dei dati solo per i contenitori nel vault di origine che non sono ancora stati spostati.</span><span class="sxs-lookup"><span data-stu-id="fc488-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="fc488-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="fc488-123">-SourceVault</span></span>
<span data-ttu-id="fc488-124">L'oggetto vault di origine da spostare.</span><span class="sxs-lookup"><span data-stu-id="fc488-124">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="fc488-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="fc488-125">-TargetVault</span></span>
<span data-ttu-id="fc488-126">Oggetto vault di destinazione in cui devono essere spostati i dati.</span><span class="sxs-lookup"><span data-stu-id="fc488-126">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="fc488-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc488-127">CommonParameters</span></span>
<span data-ttu-id="fc488-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc488-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc488-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc488-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc488-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc488-130">INPUTS</span></span>

### <span data-ttu-id="fc488-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="fc488-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="fc488-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc488-132">OUTPUTS</span></span>

### <span data-ttu-id="fc488-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fc488-133">System.String</span></span>

## <span data-ttu-id="fc488-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc488-134">NOTES</span></span>

## <span data-ttu-id="fc488-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc488-135">RELATED LINKS</span></span>
