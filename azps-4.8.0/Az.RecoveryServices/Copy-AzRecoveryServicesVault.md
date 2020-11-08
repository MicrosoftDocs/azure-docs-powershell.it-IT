---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032848"
---
# <span data-ttu-id="922b0-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="922b0-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="922b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="922b0-102">SYNOPSIS</span></span>
<span data-ttu-id="922b0-103">Copia i dati da un Vault in un'area geografica in un caveau di un'altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="922b0-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="922b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="922b0-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="922b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="922b0-105">DESCRIPTION</span></span>
<span data-ttu-id="922b0-106">Il cmdlet **Copy-AzRecoveryServicesVault** copia i dati da un Vault in un'area geografica in un Vault in un'altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="922b0-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="922b0-107">Attualmente è supportata solo la migrazione dei dati a livello di volta.</span><span class="sxs-lookup"><span data-stu-id="922b0-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="922b0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="922b0-108">EXAMPLES</span></span>

### <span data-ttu-id="922b0-109">Esempio 1: copiare i dati da vault1 a vault2</span><span class="sxs-lookup"><span data-stu-id="922b0-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="922b0-110">-Force</span><span class="sxs-lookup"><span data-stu-id="922b0-110">-Force</span></span>
<span data-ttu-id="922b0-111">Impone l'operazione di trasferimento dati (impedisce la finestra di dialogo di conferma) senza chiedere conferma per il tipo di ridondanza dello spazio di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="922b0-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="922b0-112">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="922b0-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="922b0-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="922b0-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="922b0-114">Parametro switch per provare lo spostamento dei dati solo per i contenitori nel caveau di origine che non sono ancora stati spostati.</span><span class="sxs-lookup"><span data-stu-id="922b0-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="922b0-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="922b0-115">-SourceVault</span></span>
<span data-ttu-id="922b0-116">Oggetto del Vault di origine da spostare.</span><span class="sxs-lookup"><span data-stu-id="922b0-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="922b0-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="922b0-117">-TargetVault</span></span>
<span data-ttu-id="922b0-118">Oggetto Vault di destinazione in cui devono essere spostati i dati.</span><span class="sxs-lookup"><span data-stu-id="922b0-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="922b0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922b0-119">CommonParameters</span></span>
<span data-ttu-id="922b0-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922b0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922b0-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="922b0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922b0-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="922b0-122">INPUTS</span></span>

### <span data-ttu-id="922b0-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="922b0-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="922b0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="922b0-124">OUTPUTS</span></span>

### <span data-ttu-id="922b0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="922b0-125">System.String</span></span>

## <span data-ttu-id="922b0-126">Note</span><span class="sxs-lookup"><span data-stu-id="922b0-126">NOTES</span></span>

## <span data-ttu-id="922b0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="922b0-127">RELATED LINKS</span></span>
