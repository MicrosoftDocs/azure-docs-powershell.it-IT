---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 22d2f4617e5b8a268de8518695d5217191a211df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521655"
---
# <span data-ttu-id="c8c89-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c8c89-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="c8c89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8c89-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c89-103">Concede l'accesso RDP al cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="c8c89-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8c89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8c89-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8c89-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8c89-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c89-106">Il cmdlet **Grant-AzureRmHDInsightRdpServicesAccess** consente il protocollo RDP (Remote Desktop Protocol) per accedere a un cluster di HDInsight Azure basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="c8c89-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c8c89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8c89-107">EXAMPLES</span></span>

### <span data-ttu-id="c8c89-108">Esempio 1: concedere l'accesso RDP a un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="c8c89-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="c8c89-109">Questo comando concede l'accesso RDP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="c8c89-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c8c89-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8c89-110">PARAMETERS</span></span>

### <span data-ttu-id="c8c89-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c8c89-111">-ClusterName</span></span>
<span data-ttu-id="c8c89-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c8c89-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c89-113">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="c8c89-113">-RdpAccessExpiry</span></span>
<span data-ttu-id="c8c89-114">Specifica la scadenza, come oggetto **DateTime** , per l'accesso RDP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="c8c89-114">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c89-115">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="c8c89-115">-RdpCredential</span></span>
<span data-ttu-id="c8c89-116">Specifica le credenziali RDP per il cluster.</span><span class="sxs-lookup"><span data-stu-id="c8c89-116">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="c8c89-117">Questo è solo per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="c8c89-117">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c89-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c89-118">-ResourceGroupName</span></span>
<span data-ttu-id="c8c89-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c8c89-119">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c89-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c89-120">-DefaultProfile</span></span>
<span data-ttu-id="c8c89-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c89-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8c89-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c89-122">CommonParameters</span></span>
<span data-ttu-id="c8c89-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c89-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c89-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c89-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c89-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8c89-125">INPUTS</span></span>

## <span data-ttu-id="c8c89-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8c89-126">OUTPUTS</span></span>

### <span data-ttu-id="c8c89-127">System. void</span><span class="sxs-lookup"><span data-stu-id="c8c89-127">System.Void</span></span>

## <span data-ttu-id="c8c89-128">Note</span><span class="sxs-lookup"><span data-stu-id="c8c89-128">NOTES</span></span>

## <span data-ttu-id="c8c89-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8c89-129">RELATED LINKS</span></span>

[<span data-ttu-id="c8c89-130">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c8c89-130">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


