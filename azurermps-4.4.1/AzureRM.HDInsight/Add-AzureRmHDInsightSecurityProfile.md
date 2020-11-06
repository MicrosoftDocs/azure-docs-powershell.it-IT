---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 7ea9f9d9bb07cae6db62c51b9d496f7117eee700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520524"
---
# <span data-ttu-id="0c2ce-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="0c2ce-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="0c2ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2ce-103">Aggiunge un oggetto di configurazione del cluster di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c2ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c2ce-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c2ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="0c2ce-106">Il profilo di sicurezza viene usato per creare un cluster sicuro kerberizing.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="0c2ce-107">Il profilo di sicurezza contiene la configurazione correlata all'aggiunta del cluster al dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="0c2ce-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c2ce-108">EXAMPLES</span></span>

### <span data-ttu-id="0c2ce-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c2ce-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0c2ce-110">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="0c2ce-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="0c2ce-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c2ce-111">PARAMETERS</span></span>

### <span data-ttu-id="0c2ce-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="0c2ce-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="0c2ce-113">Nomi distinti dei gruppi di Active Directory che saranno disponibili in Ambari e Ranger</span><span class="sxs-lookup"><span data-stu-id="0c2ce-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="0c2ce-114">-Config</span><span class="sxs-lookup"><span data-stu-id="0c2ce-114">-Config</span></span>
<span data-ttu-id="0c2ce-115">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="0c2ce-116">Questo oggetto viene creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="0c2ce-117">-Domain</span><span class="sxs-lookup"><span data-stu-id="0c2ce-117">-Domain</span></span>
<span data-ttu-id="0c2ce-118">Dominio Active Directory per il cluster</span><span class="sxs-lookup"><span data-stu-id="0c2ce-118">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="0c2ce-119">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="0c2ce-119">-DomainUserCredential</span></span>
<span data-ttu-id="0c2ce-120">Credenziali di un account utente di dominio con autorizzazioni sufficienti per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-120">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="0c2ce-121">Il nome utente deve essere in user@domain formato</span><span class="sxs-lookup"><span data-stu-id="0c2ce-121">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="0c2ce-122">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="0c2ce-122">-LdapsUrls</span></span>
<span data-ttu-id="0c2ce-123">URL di uno o più server LDAPs per Active Directory</span><span class="sxs-lookup"><span data-stu-id="0c2ce-123">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="0c2ce-124">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="0c2ce-124">-OrganizationalUnitDN</span></span>
<span data-ttu-id="0c2ce-125">Nome distinto dell'unità organizzativa in Active Directory in cui verranno creati gli account utente e computer</span><span class="sxs-lookup"><span data-stu-id="0c2ce-125">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="0c2ce-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c2ce-126">-Confirm</span></span>
<span data-ttu-id="0c2ce-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2ce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2ce-128">-WhatIf</span></span>
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

### <span data-ttu-id="0c2ce-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2ce-129">-DefaultProfile</span></span>
<span data-ttu-id="0c2ce-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c2ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2ce-131">CommonParameters</span></span>
<span data-ttu-id="0c2ce-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2ce-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c2ce-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2ce-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c2ce-134">INPUTS</span></span>

### <span data-ttu-id="0c2ce-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0c2ce-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="0c2ce-136">Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0c2ce-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="0c2ce-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c2ce-137">OUTPUTS</span></span>

### <span data-ttu-id="0c2ce-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="0c2ce-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="0c2ce-139">Note</span><span class="sxs-lookup"><span data-stu-id="0c2ce-139">NOTES</span></span>

## <span data-ttu-id="0c2ce-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c2ce-140">RELATED LINKS</span></span>

