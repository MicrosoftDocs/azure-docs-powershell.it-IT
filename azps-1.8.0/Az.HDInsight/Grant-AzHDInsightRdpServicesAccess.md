---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836023"
---
# <span data-ttu-id="e90eb-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e90eb-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="e90eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e90eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e90eb-103">Concede l'accesso RDP al cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="e90eb-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="e90eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e90eb-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e90eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e90eb-105">DESCRIPTION</span></span>
<span data-ttu-id="e90eb-106">Il cmdlet **Grant-AzHDInsightRdpServicesAccess** consente il protocollo RDP (Remote Desktop Protocol) per accedere a un cluster di HDInsight Azure basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="e90eb-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e90eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e90eb-107">EXAMPLES</span></span>

### <span data-ttu-id="e90eb-108">Esempio 1: concedere l'accesso RDP a un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="e90eb-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="e90eb-109">Questo comando concede l'accesso RDP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e90eb-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e90eb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e90eb-110">PARAMETERS</span></span>

### <span data-ttu-id="e90eb-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e90eb-111">-ClusterName</span></span>
<span data-ttu-id="e90eb-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e90eb-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e90eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90eb-113">-DefaultProfile</span></span>
<span data-ttu-id="e90eb-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e90eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e90eb-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="e90eb-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="e90eb-116">Specifica la scadenza, come oggetto **DateTime** , per l'accesso RDP a un cluster.</span><span class="sxs-lookup"><span data-stu-id="e90eb-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="e90eb-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="e90eb-117">-RdpCredential</span></span>
<span data-ttu-id="e90eb-118">Specifica le credenziali RDP per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e90eb-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="e90eb-119">Questo è solo per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="e90eb-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="e90eb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90eb-120">-ResourceGroupName</span></span>
<span data-ttu-id="e90eb-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e90eb-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e90eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90eb-122">CommonParameters</span></span>
<span data-ttu-id="e90eb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e90eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90eb-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90eb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90eb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e90eb-125">INPUTS</span></span>

### <span data-ttu-id="e90eb-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e90eb-126">None</span></span>

## <span data-ttu-id="e90eb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e90eb-127">OUTPUTS</span></span>

### <span data-ttu-id="e90eb-128">System. void</span><span class="sxs-lookup"><span data-stu-id="e90eb-128">System.Void</span></span>

## <span data-ttu-id="e90eb-129">Note</span><span class="sxs-lookup"><span data-stu-id="e90eb-129">NOTES</span></span>

## <span data-ttu-id="e90eb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e90eb-130">RELATED LINKS</span></span>

[<span data-ttu-id="e90eb-131">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e90eb-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


