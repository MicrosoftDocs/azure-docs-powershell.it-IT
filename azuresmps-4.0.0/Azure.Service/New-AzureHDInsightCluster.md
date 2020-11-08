---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023881"
---
# <span data-ttu-id="af665-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="af665-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="af665-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af665-102">SYNOPSIS</span></span>
<span data-ttu-id="af665-103">Crea un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="af665-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af665-104">SYNTAX</span></span>

### <span data-ttu-id="af665-105">Cluster per configurazione (con credenziali di sottoscrizione specifiche) (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af665-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="af665-106">Cluster per nome (con credenziali di sottoscrizione specifiche)</span><span class="sxs-lookup"><span data-stu-id="af665-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="af665-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af665-107">DESCRIPTION</span></span>
<span data-ttu-id="af665-108">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="af665-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="af665-109">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="af665-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="af665-110">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="af665-111">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="af665-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="af665-112">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="af665-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="af665-113">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="af665-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="af665-114">Il cmdlet **New-AzureHDInsightCluster** crea un cluster HDInsight di Azure usando i parametri specificati o usando un oggetto Configuration creato usando il cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="af665-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="af665-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af665-115">EXAMPLES</span></span>

### <span data-ttu-id="af665-116">Esempio 1: creare un cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="af665-116">Example 1: Create an HDInsight cluster</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="af665-117">Questo esempio crea un cluster HDInsight per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="af665-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="af665-118">Il primo comando usa il cmdlet **Get-AzureSubscription** per ottenere l'ID corrente della sottoscrizione e lo archivia nella variabile $SubId.</span><span class="sxs-lookup"><span data-stu-id="af665-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="af665-119">Il secondo e il terzo comando usano il cmdlet **Get-AzureStorageKey** per ottenere le chiavi di archiviazione primarie per MyBlobStorage e MySecondBlobStorage, quindi archiviare rispettivamente le chiavi nelle variabili $Key 1 e $Key 2.</span><span class="sxs-lookup"><span data-stu-id="af665-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="af665-120">I comandi quarto, quinto e sesto usano il cmdlet **Get-Credential** per ottenere le credenziali per l'abbonamento corrente e per oozie e hive e quindi archiviare le credenziali nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="af665-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="af665-121">Il comando finale esegue una sequenza di operazioni usando questi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="af665-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="af665-122">**New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="af665-123">**Set-AzureHDInsightDefaultStorage** per impostare l'account di archiviazione predefinito per la configurazione su MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="af665-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="af665-124">**Add-AzureHDInsightStorage** per aggiungere un secondo account di archiviazione denominato MySecondBlobStorage.blob.Core.Windows.NET alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="af665-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="af665-125">**Add-AzureHDInsightMetastore** per aggiungere un Metastore per oozie e un Metastore per hive alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="af665-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="af665-126">**New-AzureHDInsightCluster** per creare un cluster HDInsight con la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="af665-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="af665-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af665-127">PARAMETERS</span></span>

### <span data-ttu-id="af665-128">-Certificato</span><span class="sxs-lookup"><span data-stu-id="af665-128">-Certificate</span></span>
<span data-ttu-id="af665-129">Specifica il certificato di gestione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="af665-129">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="af665-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="af665-131">Specifica il numero di nodi dati da creare per un cluster.</span><span class="sxs-lookup"><span data-stu-id="af665-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-132">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="af665-132">-ClusterType</span></span>
<span data-ttu-id="af665-133">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="af665-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-134">-Config</span><span class="sxs-lookup"><span data-stu-id="af665-134">-Config</span></span>
<span data-ttu-id="af665-135">Specifica un oggetto Configuration creato usando il cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="af665-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af665-136">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="af665-136">-Credential</span></span>
<span data-ttu-id="af665-137">Specifica le credenziali utente per HDInsight da usare per l'account predefinito usato per accedere in remoto a un cluster Hadoop.</span><span class="sxs-lookup"><span data-stu-id="af665-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="af665-138">Queste credenziali sono distinte dalle credenziali di sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="af665-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="af665-139">-DataNodeVMSize</span></span>
<span data-ttu-id="af665-140">Specifica le dimensioni della macchina virtuale per il nodo dati.</span><span class="sxs-lookup"><span data-stu-id="af665-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="af665-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="af665-142">Specifica la chiave dell'account per l'account di archiviazione predefinito usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="af665-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="af665-144">Specifica il nome dell'account di archiviazione predefinito usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="af665-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="af665-146">Specifica il nome del contenitore predefinito nell'account di archiviazione di Azure predefinito usato da un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-147">-EndPoint</span><span class="sxs-lookup"><span data-stu-id="af665-147">-EndPoint</span></span>
<span data-ttu-id="af665-148">Specifica l'endpoint da usare per la connessione a Azure.</span><span class="sxs-lookup"><span data-stu-id="af665-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="af665-149">Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.</span><span class="sxs-lookup"><span data-stu-id="af665-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="af665-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="af665-151">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="af665-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="af665-152">-HostedService</span></span>
<span data-ttu-id="af665-153">Specifica lo spazio dei nomi di un servizio HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="af665-154">Se non specifichi questo parametro, questo cmdlet usa lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="af665-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="af665-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="af665-156">Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="af665-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-157">-Posizione</span><span class="sxs-lookup"><span data-stu-id="af665-157">-Location</span></span>
<span data-ttu-id="af665-158">Specifica l'area geografica in cui creare un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="af665-159">-Name</span></span>
<span data-ttu-id="af665-160">Specifica il nome del cluster di Azure HDInsight da creare.</span><span class="sxs-lookup"><span data-stu-id="af665-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="af665-161">-OSType</span></span>
<span data-ttu-id="af665-162">Specifica il sistema operativo per un cluster.</span><span class="sxs-lookup"><span data-stu-id="af665-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-163">-Profile</span><span class="sxs-lookup"><span data-stu-id="af665-163">-Profile</span></span>
<span data-ttu-id="af665-164">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af665-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af665-165">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="af665-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="af665-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="af665-167">Specifica la scadenza, come oggetto **DateTime** , per l'accesso RDP (Remote Desktop Protocol) a un cluster.</span><span class="sxs-lookup"><span data-stu-id="af665-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="af665-168">-RdpCredential</span></span>
<span data-ttu-id="af665-169">Specifica le credenziali per l'accesso RDP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="af665-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="af665-170">-SshCredential</span></span>
<span data-ttu-id="af665-171">Specifica il nome utente e la password di Secure Shell (SSH) per il cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="af665-172">Questo parametro è valido solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="af665-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="af665-173">-SshPublicKey</span></span>
<span data-ttu-id="af665-174">Specifica la chiave pubblica SSH per un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="af665-175">Questo parametro è valido solo per i cluster Linux.</span><span class="sxs-lookup"><span data-stu-id="af665-175">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="af665-176">-SubnetName</span></span>
<span data-ttu-id="af665-177">Specifica il nome di una subnet.</span><span class="sxs-lookup"><span data-stu-id="af665-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-178">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="af665-178">-Subscription</span></span>
<span data-ttu-id="af665-179">Specifica l'abbonamento a Azure in cui creare un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af665-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-180">-Versione</span><span class="sxs-lookup"><span data-stu-id="af665-180">-Version</span></span>
<span data-ttu-id="af665-181">Specifica la versione del cluster HDInsight da creare.</span><span class="sxs-lookup"><span data-stu-id="af665-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="af665-182">-VirtualNetworkId</span></span>
<span data-ttu-id="af665-183">Specifica l'ID della rete virtuale in cui eseguire il provisioning del cluster.</span><span class="sxs-lookup"><span data-stu-id="af665-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="af665-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="af665-185">Specifica le dimensioni della macchina virtuale per il nodo ZooKeeper.</span><span class="sxs-lookup"><span data-stu-id="af665-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="af665-186">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="af665-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af665-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af665-187">CommonParameters</span></span>
<span data-ttu-id="af665-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af665-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af665-189">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af665-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af665-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af665-190">INPUTS</span></span>

## <span data-ttu-id="af665-191">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af665-191">OUTPUTS</span></span>

## <span data-ttu-id="af665-192">Note</span><span class="sxs-lookup"><span data-stu-id="af665-192">NOTES</span></span>

## <span data-ttu-id="af665-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af665-193">RELATED LINKS</span></span>

[<span data-ttu-id="af665-194">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="af665-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="af665-195">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="af665-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="af665-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="af665-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="af665-197">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="af665-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="af665-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="af665-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="af665-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="af665-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="af665-200">Usare-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="af665-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


