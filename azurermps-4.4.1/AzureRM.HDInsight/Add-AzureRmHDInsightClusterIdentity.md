---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: fc992b427e0c07b1f9db634f9369c21917ec9556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688640"
---
# <span data-ttu-id="55ffb-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="55ffb-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="55ffb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="55ffb-103">Aggiunge un'identità cluster a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="55ffb-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55ffb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55ffb-104">SYNTAX</span></span>

### <span data-ttu-id="55ffb-105">CertificateFilePath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55ffb-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55ffb-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="55ffb-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ffb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55ffb-107">DESCRIPTION</span></span>
<span data-ttu-id="55ffb-108">Il cmdlet **Add-AzureRmHDInsightClusterIdentity** aggiunge un'identità cluster all'oggetto di configurazione di Azure HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="55ffb-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="55ffb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55ffb-109">EXAMPLES</span></span>

### <span data-ttu-id="55ffb-110">Esempio 1: aggiungere informazioni sull'identità del cluster all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="55ffb-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="55ffb-111">Questo comando aggiunge le informazioni sull'identità del cluster al cluster denominato your-Hadoop-001, consentendo al cluster di accedere a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55ffb-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="55ffb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55ffb-112">PARAMETERS</span></span>

### <span data-ttu-id="55ffb-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="55ffb-113">-AadTenantId</span></span>
<span data-ttu-id="55ffb-114">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55ffb-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ffb-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="55ffb-115">-CertificateFileContents</span></span>
<span data-ttu-id="55ffb-116">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55ffb-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ffb-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="55ffb-117">-CertificateFilePath</span></span>
<span data-ttu-id="55ffb-118">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="55ffb-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="55ffb-119">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55ffb-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ffb-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="55ffb-120">-CertificatePassword</span></span>
<span data-ttu-id="55ffb-121">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="55ffb-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="55ffb-122">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55ffb-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ffb-123">-Config</span><span class="sxs-lookup"><span data-stu-id="55ffb-123">-Config</span></span>
<span data-ttu-id="55ffb-124">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55ffb-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="55ffb-125">Questo oggetto viene creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="55ffb-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55ffb-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="55ffb-126">-ObjectId</span></span>
<span data-ttu-id="55ffb-127">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="55ffb-127">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="55ffb-128">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55ffb-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55ffb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ffb-129">-DefaultProfile</span></span>
<span data-ttu-id="55ffb-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55ffb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55ffb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ffb-131">CommonParameters</span></span>
<span data-ttu-id="55ffb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ffb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ffb-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ffb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ffb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55ffb-134">INPUTS</span></span>

### <span data-ttu-id="55ffb-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="55ffb-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="55ffb-136">Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="55ffb-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="55ffb-137">GUID</span><span class="sxs-lookup"><span data-stu-id="55ffb-137">Guid</span></span>
<span data-ttu-id="55ffb-138">Il parametro "ObjectId" accetta il valore di tipo "GUID" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="55ffb-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="55ffb-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55ffb-139">OUTPUTS</span></span>

### <span data-ttu-id="55ffb-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="55ffb-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="55ffb-141">Note</span><span class="sxs-lookup"><span data-stu-id="55ffb-141">NOTES</span></span>

## <span data-ttu-id="55ffb-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55ffb-142">RELATED LINKS</span></span>

[<span data-ttu-id="55ffb-143">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="55ffb-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


