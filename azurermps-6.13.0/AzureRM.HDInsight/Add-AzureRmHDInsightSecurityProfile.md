---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 003072e6821561c78975d50fa627edf0f7fd120a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515323"
---
# <span data-ttu-id="4ebf2-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4ebf2-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="4ebf2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ebf2-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebf2-103">Aggiunge un oggetto di configurazione del cluster di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ebf2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ebf2-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ebf2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ebf2-105">DESCRIPTION</span></span>
<span data-ttu-id="4ebf2-106">Il profilo di sicurezza viene usato per creare un cluster sicuro kerberizing.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="4ebf2-107">Il profilo di sicurezza contiene la configurazione correlata all'aggiunta del cluster al dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="4ebf2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ebf2-108">EXAMPLES</span></span>

### <span data-ttu-id="4ebf2-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ebf2-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4ebf2-110">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="4ebf2-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="4ebf2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ebf2-111">PARAMETERS</span></span>

### <span data-ttu-id="4ebf2-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="4ebf2-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="4ebf2-113">Nomi distinti dei gruppi di Active Directory che saranno disponibili in Ambari e Ranger</span><span class="sxs-lookup"><span data-stu-id="4ebf2-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="4ebf2-114">-Config</span><span class="sxs-lookup"><span data-stu-id="4ebf2-114">-Config</span></span>
<span data-ttu-id="4ebf2-115">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4ebf2-116">Questo oggetto viene creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="4ebf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebf2-117">-DefaultProfile</span></span>
<span data-ttu-id="4ebf2-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4ebf2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ebf2-119">-Domain</span><span class="sxs-lookup"><span data-stu-id="4ebf2-119">-Domain</span></span>
<span data-ttu-id="4ebf2-120">Dominio Active Directory per il cluster</span><span class="sxs-lookup"><span data-stu-id="4ebf2-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="4ebf2-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="4ebf2-121">-DomainUserCredential</span></span>
<span data-ttu-id="4ebf2-122">Credenziali di un account utente di dominio con autorizzazioni sufficienti per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="4ebf2-123">Il nome utente deve essere in user@domain formato</span><span class="sxs-lookup"><span data-stu-id="4ebf2-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="4ebf2-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="4ebf2-124">-LdapsUrls</span></span>
<span data-ttu-id="4ebf2-125">URL di uno o più server LDAPs per Active Directory</span><span class="sxs-lookup"><span data-stu-id="4ebf2-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="4ebf2-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="4ebf2-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="4ebf2-127">Nome distinto dell'unità organizzativa in Active Directory in cui verranno creati gli account utente e computer</span><span class="sxs-lookup"><span data-stu-id="4ebf2-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="4ebf2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ebf2-128">-Confirm</span></span>
<span data-ttu-id="4ebf2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ebf2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ebf2-130">-WhatIf</span></span>
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

### <span data-ttu-id="4ebf2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebf2-131">CommonParameters</span></span>
<span data-ttu-id="4ebf2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebf2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebf2-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebf2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebf2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ebf2-134">INPUTS</span></span>

### <span data-ttu-id="4ebf2-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4ebf2-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="4ebf2-136">Parametri: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ebf2-136">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="4ebf2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ebf2-137">OUTPUTS</span></span>

### <span data-ttu-id="4ebf2-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4ebf2-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="4ebf2-139">Note</span><span class="sxs-lookup"><span data-stu-id="4ebf2-139">NOTES</span></span>

## <span data-ttu-id="4ebf2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ebf2-140">RELATED LINKS</span></span>
