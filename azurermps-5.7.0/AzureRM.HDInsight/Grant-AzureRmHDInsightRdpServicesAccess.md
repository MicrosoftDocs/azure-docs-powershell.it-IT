---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 09b389763897f91a23f56f0a3383dd3f7f03ca1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685834"
---
# <span data-ttu-id="b2779-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b2779-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="b2779-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2779-102">SYNOPSIS</span></span>
<span data-ttu-id="b2779-103">Concede l'accesso RDP al cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="b2779-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2779-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2779-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2779-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2779-105">DESCRIPTION</span></span>
<span data-ttu-id="b2779-106">Il cmdlet **Grant-AzureRmHDInsightRdpServicesAccess** consente il protocollo RDP (Remote Desktop Protocol) per accedere a un cluster di HDInsight Azure basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="b2779-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b2779-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2779-107">EXAMPLES</span></span>

### <span data-ttu-id="b2779-108">Esempio 1: concedere l'accesso RDP a un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="b2779-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="b2779-109">Questo comando concede l'accesso RDP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b2779-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b2779-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2779-110">PARAMETERS</span></span>

### <span data-ttu-id="b2779-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b2779-111">-ClusterName</span></span>
<span data-ttu-id="b2779-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="b2779-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2779-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2779-113">-DefaultProfile</span></span>
<span data-ttu-id="b2779-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2779-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2779-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="b2779-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="b2779-116">Specifica la scadenza, come oggetto **DateTime** , per l'accesso RDP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="b2779-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2779-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="b2779-117">-RdpCredential</span></span>
<span data-ttu-id="b2779-118">Specifica le credenziali RDP per il cluster.</span><span class="sxs-lookup"><span data-stu-id="b2779-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="b2779-119">Questo è solo per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="b2779-119">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2779-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2779-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2779-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2779-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b2779-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2779-122">CommonParameters</span></span>
<span data-ttu-id="b2779-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2779-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2779-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2779-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2779-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2779-125">INPUTS</span></span>

### <span data-ttu-id="b2779-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b2779-126">None</span></span>
<span data-ttu-id="b2779-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b2779-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2779-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2779-128">OUTPUTS</span></span>

### <span data-ttu-id="b2779-129">System. void</span><span class="sxs-lookup"><span data-stu-id="b2779-129">System.Void</span></span>

## <span data-ttu-id="b2779-130">Note</span><span class="sxs-lookup"><span data-stu-id="b2779-130">NOTES</span></span>

## <span data-ttu-id="b2779-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2779-131">RELATED LINKS</span></span>

[<span data-ttu-id="b2779-132">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b2779-132">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


