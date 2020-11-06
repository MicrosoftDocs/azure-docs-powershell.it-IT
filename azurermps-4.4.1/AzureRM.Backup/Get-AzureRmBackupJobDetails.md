---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: f9f0808db919ad5d1d38b29daa720fb9b8a5baee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511336"
---
# <span data-ttu-id="1c54e-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="1c54e-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="1c54e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c54e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c54e-103">Ottiene i dettagli di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="1c54e-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c54e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c54e-104">SYNTAX</span></span>

### <span data-ttu-id="1c54e-105">JobsFiltersSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c54e-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c54e-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="1c54e-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c54e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c54e-107">DESCRIPTION</span></span>
<span data-ttu-id="1c54e-108">Il cmdlet **Get-AzureRmBackupJobDetails** ottiene i dettagli di un processo di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c54e-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="1c54e-109">Puoi usare questo cmdlet per raccogliere informazioni su un processo che non riesce.</span><span class="sxs-lookup"><span data-stu-id="1c54e-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="1c54e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c54e-110">EXAMPLES</span></span>

### <span data-ttu-id="1c54e-111">Esempio 1: visualizzare i dettagli di un processo non riuscito</span><span class="sxs-lookup"><span data-stu-id="1c54e-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="1c54e-112">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="1c54e-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="1c54e-113">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="1c54e-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="1c54e-114">Il secondo comando consente di ottenere processi non riusciti dalla volta in $Vault e quindi di archiviarli nella variabile di matrice $Jobs.</span><span class="sxs-lookup"><span data-stu-id="1c54e-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="1c54e-115">Il terzo processo ottiene i dettagli per il primo processo nella variabile $Jobs e quindi archivia tali dettagli nella variabile $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="1c54e-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="1c54e-116">Il comando finale Visualizza la proprietà **ErrorDetails** di $JobDetails usando la sintassi dei punti standard.</span><span class="sxs-lookup"><span data-stu-id="1c54e-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="1c54e-117">Esempio 2: visualizzare l'azione consigliata per un processo non riuscito</span><span class="sxs-lookup"><span data-stu-id="1c54e-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="1c54e-118">Questo comando Visualizza l'azione consigliata dalla variabile $JobDetails creata nel primo esempio.</span><span class="sxs-lookup"><span data-stu-id="1c54e-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="1c54e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c54e-119">PARAMETERS</span></span>

### <span data-ttu-id="1c54e-120">-Job</span><span class="sxs-lookup"><span data-stu-id="1c54e-120">-Job</span></span>
<span data-ttu-id="1c54e-121">Specifica un processo per cui questo cmdlet ottiene i dettagli.</span><span class="sxs-lookup"><span data-stu-id="1c54e-121">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="1c54e-122">Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="1c54e-122">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c54e-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="1c54e-123">-JobId</span></span>
<span data-ttu-id="1c54e-124">Specifica l'ID di un processo per cui questo cmdlet ottiene i dettagli.</span><span class="sxs-lookup"><span data-stu-id="1c54e-124">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="1c54e-125">L'ID è la proprietà **InstanceID** di un oggetto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="1c54e-125">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="1c54e-126">Per ottenere un oggetto **AzureRmBackupJob** , USA Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="1c54e-126">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c54e-127">-Vault</span><span class="sxs-lookup"><span data-stu-id="1c54e-127">-Vault</span></span>
<span data-ttu-id="1c54e-128">Specifica il Vault di backup per cui questo cmdlet ottiene i dettagli del processo.</span><span class="sxs-lookup"><span data-stu-id="1c54e-128">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="1c54e-129">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="1c54e-129">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c54e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c54e-130">-DefaultProfile</span></span>
<span data-ttu-id="1c54e-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c54e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c54e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c54e-132">CommonParameters</span></span>
<span data-ttu-id="1c54e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c54e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c54e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c54e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c54e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c54e-135">INPUTS</span></span>

### <span data-ttu-id="1c54e-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1c54e-136">None</span></span>

## <span data-ttu-id="1c54e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c54e-137">OUTPUTS</span></span>

### <span data-ttu-id="1c54e-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="1c54e-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="1c54e-139">Note</span><span class="sxs-lookup"><span data-stu-id="1c54e-139">NOTES</span></span>
* <span data-ttu-id="1c54e-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1c54e-140">None</span></span>

## <span data-ttu-id="1c54e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c54e-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c54e-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="1c54e-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="1c54e-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="1c54e-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


