---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 1f841d8cb49463f1ca9ce9198fc6173bb7efe506
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190723"
---
# <span data-ttu-id="07dd5-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="07dd5-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="07dd5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="07dd5-103">Aggiunge un profilo di sicurezza a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="07dd5-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="07dd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07dd5-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07dd5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="07dd5-106">Il profilo di sicurezza viene usato per creare un cluster sicuro kerberizing.</span><span class="sxs-lookup"><span data-stu-id="07dd5-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="07dd5-107">Il profilo di sicurezza contiene la configurazione correlata all'aggiunta del cluster al dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07dd5-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="07dd5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07dd5-108">EXAMPLES</span></span>

### <span data-ttu-id="07dd5-109">Esempio 1: aggiungere il profilo di sicurezza all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="07dd5-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
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

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="07dd5-110">Questo comando aggiunge un valore del profilo di sicurezza al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="07dd5-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="07dd5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07dd5-111">PARAMETERS</span></span>

### <span data-ttu-id="07dd5-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="07dd5-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="07dd5-113">Nomi distinti dei gruppi di Active Directory che saranno disponibili in Ambari e Ranger</span><span class="sxs-lookup"><span data-stu-id="07dd5-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07dd5-114">-Config</span><span class="sxs-lookup"><span data-stu-id="07dd5-114">-Config</span></span>
<span data-ttu-id="07dd5-115">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07dd5-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="07dd5-116">Questo oggetto viene creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="07dd5-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="07dd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07dd5-117">-DefaultProfile</span></span>
<span data-ttu-id="07dd5-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="07dd5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07dd5-119">-Domain</span><span class="sxs-lookup"><span data-stu-id="07dd5-119">-Domain</span></span>
<span data-ttu-id="07dd5-120">Dominio Active Directory per il cluster</span><span class="sxs-lookup"><span data-stu-id="07dd5-120">Active Directory domain for the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07dd5-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="07dd5-121">-DomainUserCredential</span></span>
<span data-ttu-id="07dd5-122">Credenziali di un account utente di dominio con autorizzazioni sufficienti per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="07dd5-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="07dd5-123">Il nome utente deve essere in user@domain formato</span><span class="sxs-lookup"><span data-stu-id="07dd5-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07dd5-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="07dd5-124">-LdapsUrls</span></span>
<span data-ttu-id="07dd5-125">URL di uno o più server LDAPs per Active Directory</span><span class="sxs-lookup"><span data-stu-id="07dd5-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07dd5-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="07dd5-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="07dd5-127">Nome distinto dell'unità organizzativa in Active Directory in cui verranno creati gli account utente e computer</span><span class="sxs-lookup"><span data-stu-id="07dd5-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07dd5-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07dd5-128">-Confirm</span></span>
<span data-ttu-id="07dd5-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07dd5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07dd5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07dd5-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07dd5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07dd5-131">CommonParameters</span></span>
<span data-ttu-id="07dd5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07dd5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07dd5-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07dd5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07dd5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07dd5-134">INPUTS</span></span>

### <span data-ttu-id="07dd5-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="07dd5-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="07dd5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07dd5-136">OUTPUTS</span></span>

### <span data-ttu-id="07dd5-137">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="07dd5-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="07dd5-138">Note</span><span class="sxs-lookup"><span data-stu-id="07dd5-138">NOTES</span></span>

## <span data-ttu-id="07dd5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07dd5-139">RELATED LINKS</span></span>