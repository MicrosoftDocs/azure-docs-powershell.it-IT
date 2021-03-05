---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: c2dd4abcf9e917d4a34ed548cd356e02875971b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994768"
---
# <span data-ttu-id="dc244-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="dc244-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="dc244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc244-102">SYNOPSIS</span></span>
<span data-ttu-id="dc244-103">Richiama il failover di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dc244-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="dc244-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc244-104">SYNTAX</span></span>

### <span data-ttu-id="dc244-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc244-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc244-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="dc244-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc244-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dc244-107">DESCRIPTION</span></span>
<span data-ttu-id="dc244-108">Richiama il failover di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dc244-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="dc244-109">La richiesta di failover può essere attivata per un account di archiviazione in caso di problemi di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="dc244-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="dc244-110">Il failover si verifica dal cluster primario dell'account di archiviazione al cluster secondario per gli account RA-GRS.</span><span class="sxs-lookup"><span data-stu-id="dc244-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="dc244-111">Il cluster secondario diventerà primario dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc244-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="dc244-112">Prima di avviare il failover, tenere conto dell'impatto seguente sull'account di archiviazione: 1.1.</span><span class="sxs-lookup"><span data-stu-id="dc244-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="dc244-113">Controlla la data/ora dell'ultima sincronizzazione con GET BLOB https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats) Service Stats (, GET Table Service Stats ( https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) e GET Queue Service Stats ( per il https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) tuo account).</span><span class="sxs-lookup"><span data-stu-id="dc244-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="dc244-114">Si tratta dei dati che si potrebbero perdere se si avvia il failover.</span><span class="sxs-lookup"><span data-stu-id="dc244-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="dc244-115">2.Dopo il failover, il tipo di account di archiviazione verrà convertito in archiviazione ridondante locale(LRS).</span><span class="sxs-lookup"><span data-stu-id="dc244-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="dc244-116">È possibile convertire l'account in modo da usare un sistema di archiviazione geo-ridondante (GRS).</span><span class="sxs-lookup"><span data-stu-id="dc244-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="dc244-117">3.Dopo aver ri abilitato il GRS per l'account di archiviazione, Microsoft replica i dati nella nuova area secondaria.</span><span class="sxs-lookup"><span data-stu-id="dc244-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="dc244-118">Il tempo di replica dipende dalla quantità di dati da replicare.</span><span class="sxs-lookup"><span data-stu-id="dc244-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="dc244-119">Tenere presente che ci sono costi di larghezza di banda per il bootstrap.</span><span class="sxs-lookup"><span data-stu-id="dc244-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="dc244-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="dc244-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="dc244-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc244-121">EXAMPLES</span></span>

### <span data-ttu-id="dc244-122">Esempio 1: Richiamare il failover di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dc244-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="dc244-123">Questo comando controlla l'ultima ora di sincronizzazione di un account di archiviazione e quindi richiama il failover. Il cluster secondario diventerà primario dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc244-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="dc244-124">Poiché il failover richiede molto tempo, è consigliabile eseguirlo nel back-end con il parametro -Asjob e quindi attendere il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="dc244-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="dc244-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc244-125">PARAMETERS</span></span>

### <span data-ttu-id="dc244-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc244-126">-AsJob</span></span>
<span data-ttu-id="dc244-127">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dc244-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc244-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc244-128">-DefaultProfile</span></span>
<span data-ttu-id="dc244-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc244-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc244-130">-Force</span><span class="sxs-lookup"><span data-stu-id="dc244-130">-Force</span></span>
<span data-ttu-id="dc244-131">Forzare il failover dell'account</span><span class="sxs-lookup"><span data-stu-id="dc244-131">Force to Failover the Account</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc244-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc244-132">-InputObject</span></span>
<span data-ttu-id="dc244-133">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dc244-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc244-134">-Name</span><span class="sxs-lookup"><span data-stu-id="dc244-134">-Name</span></span>
<span data-ttu-id="dc244-135">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dc244-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc244-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc244-136">-ResourceGroupName</span></span>
<span data-ttu-id="dc244-137">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc244-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc244-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc244-138">-Confirm</span></span>
<span data-ttu-id="dc244-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc244-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc244-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc244-140">-WhatIf</span></span>
<span data-ttu-id="dc244-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc244-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc244-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc244-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc244-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc244-143">CommonParameters</span></span>
<span data-ttu-id="dc244-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc244-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc244-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc244-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc244-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="dc244-146">INPUTS</span></span>

### <span data-ttu-id="dc244-147">System.String</span><span class="sxs-lookup"><span data-stu-id="dc244-147">System.String</span></span>

## <span data-ttu-id="dc244-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc244-148">OUTPUTS</span></span>

### <span data-ttu-id="dc244-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc244-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dc244-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="dc244-150">NOTES</span></span>

## <span data-ttu-id="dc244-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc244-151">RELATED LINKS</span></span>
