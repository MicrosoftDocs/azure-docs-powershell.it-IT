---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 6d3924f3613d01e515e58e1b35c3640b0447ca06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209442"
---
# <span data-ttu-id="4d01f-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="4d01f-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="4d01f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d01f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d01f-103">Aggiunge un'identità del cluster a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="4d01f-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="4d01f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d01f-104">SYNTAX</span></span>

### <span data-ttu-id="4d01f-105">CertificateFilePath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d01f-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d01f-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4d01f-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d01f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d01f-107">DESCRIPTION</span></span>
<span data-ttu-id="4d01f-108">Il cmdlet **Add-AzHDInsightClusterIdentity** aggiunge un'identità cluster all'oggetto configurazione Azure HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4d01f-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4d01f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d01f-109">EXAMPLES</span></span>

### <span data-ttu-id="4d01f-110">Esempio 1: Aggiungere informazioni di identità del cluster all'oggetto configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="4d01f-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="4d01f-111">Questo comando aggiunge le informazioni di identità del cluster al cluster denominato your-hadoop-001, consentendo al cluster di accedere ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d01f-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="4d01f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d01f-112">PARAMETERS</span></span>

### <span data-ttu-id="4d01f-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="4d01f-113">-AadTenantId</span></span>
<span data-ttu-id="4d01f-114">Specifica l'ID tenant di Azure AD che verrà usato quando si accede ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d01f-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4d01f-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4d01f-115">-ApplicationId</span></span>
<span data-ttu-id="4d01f-116">ID applicazione entità servizio per l'accesso ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4d01f-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d01f-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4d01f-117">-CertificateFileContents</span></span>
<span data-ttu-id="4d01f-118">Specifica il contenuto del file del certificato che verrà usato quando si accede ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d01f-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4d01f-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4d01f-119">-CertificateFilePath</span></span>
<span data-ttu-id="4d01f-120">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4d01f-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4d01f-121">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d01f-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4d01f-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4d01f-122">-CertificatePassword</span></span>
<span data-ttu-id="4d01f-123">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4d01f-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4d01f-124">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d01f-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4d01f-125">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="4d01f-125">-Config</span></span>
<span data-ttu-id="4d01f-126">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d01f-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4d01f-127">Questo oggetto viene creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4d01f-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="4d01f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d01f-128">-DefaultProfile</span></span>
<span data-ttu-id="4d01f-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4d01f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d01f-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4d01f-130">-ObjectId</span></span>
<span data-ttu-id="4d01f-131">Specifica l'ID oggetto di Azure AD (un GUID) dell'entità servizio di Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="4d01f-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4d01f-132">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d01f-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4d01f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d01f-133">CommonParameters</span></span>
<span data-ttu-id="4d01f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d01f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d01f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d01f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d01f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d01f-136">INPUTS</span></span>

### <span data-ttu-id="4d01f-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4d01f-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="4d01f-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4d01f-138">System.Guid</span></span>

## <span data-ttu-id="4d01f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d01f-139">OUTPUTS</span></span>

### <span data-ttu-id="4d01f-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4d01f-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4d01f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d01f-141">NOTES</span></span>

## <span data-ttu-id="4d01f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d01f-142">RELATED LINKS</span></span>

[<span data-ttu-id="4d01f-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4d01f-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


