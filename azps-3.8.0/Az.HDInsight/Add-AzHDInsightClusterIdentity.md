---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: fcad97b2316e9db652fe4dc9df70bdc0f5d8b84d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022841"
---
# <span data-ttu-id="2c11c-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="2c11c-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="2c11c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c11c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c11c-103">Aggiunge un'identità cluster a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="2c11c-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="2c11c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c11c-104">SYNTAX</span></span>

### <span data-ttu-id="2c11c-105">CertificateFilePath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c11c-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c11c-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="2c11c-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c11c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c11c-107">DESCRIPTION</span></span>
<span data-ttu-id="2c11c-108">Il cmdlet **Add-AzHDInsightClusterIdentity** aggiunge un'identità cluster all'oggetto di configurazione di Azure HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="2c11c-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="2c11c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c11c-109">EXAMPLES</span></span>

### <span data-ttu-id="2c11c-110">Esempio 1: aggiungere informazioni sull'identità del cluster all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="2c11c-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="2c11c-111">Questo comando aggiunge le informazioni sull'identità del cluster al cluster denominato your-Hadoop-001, consentendo al cluster di accedere a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c11c-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="2c11c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c11c-112">PARAMETERS</span></span>

### <span data-ttu-id="2c11c-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="2c11c-113">-AadTenantId</span></span>
<span data-ttu-id="2c11c-114">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c11c-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2c11c-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2c11c-115">-ApplicationId</span></span>
<span data-ttu-id="2c11c-116">ID applicazione dell'entità servizio per l'accesso a Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2c11c-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c11c-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="2c11c-117">-CertificateFileContents</span></span>
<span data-ttu-id="2c11c-118">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c11c-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2c11c-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="2c11c-119">-CertificateFilePath</span></span>
<span data-ttu-id="2c11c-120">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="2c11c-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="2c11c-121">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c11c-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2c11c-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2c11c-122">-CertificatePassword</span></span>
<span data-ttu-id="2c11c-123">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="2c11c-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="2c11c-124">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c11c-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2c11c-125">-Config</span><span class="sxs-lookup"><span data-stu-id="2c11c-125">-Config</span></span>
<span data-ttu-id="2c11c-126">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c11c-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="2c11c-127">Questo oggetto viene creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="2c11c-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="2c11c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c11c-128">-DefaultProfile</span></span>
<span data-ttu-id="2c11c-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2c11c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c11c-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2c11c-130">-ObjectId</span></span>
<span data-ttu-id="2c11c-131">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="2c11c-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="2c11c-132">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c11c-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2c11c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c11c-133">CommonParameters</span></span>
<span data-ttu-id="2c11c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c11c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c11c-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c11c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c11c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c11c-136">INPUTS</span></span>

### <span data-ttu-id="2c11c-137">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2c11c-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="2c11c-138">System. Guid</span><span class="sxs-lookup"><span data-stu-id="2c11c-138">System.Guid</span></span>

## <span data-ttu-id="2c11c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c11c-139">OUTPUTS</span></span>

### <span data-ttu-id="2c11c-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2c11c-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="2c11c-141">Note</span><span class="sxs-lookup"><span data-stu-id="2c11c-141">NOTES</span></span>

## <span data-ttu-id="2c11c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c11c-142">RELATED LINKS</span></span>

[<span data-ttu-id="2c11c-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="2c11c-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


