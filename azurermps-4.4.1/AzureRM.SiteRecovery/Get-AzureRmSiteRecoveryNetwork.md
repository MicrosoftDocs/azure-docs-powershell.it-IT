---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512911"
---
# <span data-ttu-id="7d24e-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="7d24e-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="7d24e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d24e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d24e-103">Ottiene informazioni sulle reti gestite dal ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="7d24e-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d24e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d24e-104">SYNTAX</span></span>

### <span data-ttu-id="7d24e-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d24e-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d24e-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="7d24e-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d24e-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="7d24e-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d24e-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="7d24e-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d24e-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="7d24e-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d24e-110">ByName</span><span class="sxs-lookup"><span data-stu-id="7d24e-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d24e-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d24e-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d24e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d24e-112">DESCRIPTION</span></span>
<span data-ttu-id="7d24e-113">Il cmdlet **Get-AzureRmSiteRecoveryNetwork** ottiene informazioni sulle reti di ripristino dei siti di Azure per l'attuale archivio di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="7d24e-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7d24e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d24e-114">EXAMPLES</span></span>

## <span data-ttu-id="7d24e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d24e-115">PARAMETERS</span></span>

### <span data-ttu-id="7d24e-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="7d24e-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d24e-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d24e-117">-FriendlyName</span></span>
<span data-ttu-id="7d24e-118">Specifica il nome descrittivo della rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d24e-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d24e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d24e-119">-Name</span></span>
<span data-ttu-id="7d24e-120">Specifica il nome della rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d24e-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d24e-121">-Server</span><span class="sxs-lookup"><span data-stu-id="7d24e-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d24e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d24e-122">-DefaultProfile</span></span>
<span data-ttu-id="7d24e-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d24e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d24e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d24e-124">CommonParameters</span></span>
<span data-ttu-id="7d24e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d24e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d24e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d24e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d24e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d24e-127">INPUTS</span></span>

### <span data-ttu-id="7d24e-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7d24e-128">ASRFabric</span></span>
<span data-ttu-id="7d24e-129">Il parametro "tessuto" accetta il valore di tipo "ASRFabric" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7d24e-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="7d24e-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="7d24e-130">String</span></span>
<span data-ttu-id="7d24e-131">Il parametro "FriendlyName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7d24e-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7d24e-132">Stringa</span><span class="sxs-lookup"><span data-stu-id="7d24e-132">String</span></span>
<span data-ttu-id="7d24e-133">Il parametro "FriendlyName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7d24e-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7d24e-134">Stringa</span><span class="sxs-lookup"><span data-stu-id="7d24e-134">String</span></span>
<span data-ttu-id="7d24e-135">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7d24e-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7d24e-136">Stringa</span><span class="sxs-lookup"><span data-stu-id="7d24e-136">String</span></span>
<span data-ttu-id="7d24e-137">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7d24e-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7d24e-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="7d24e-138">ASRServer</span></span>
<span data-ttu-id="7d24e-139">Il parametro ' server ' accetta il valore di tipo ' ASRServer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7d24e-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="7d24e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d24e-140">OUTPUTS</span></span>

### <span data-ttu-id="7d24e-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="7d24e-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="7d24e-142">Note</span><span class="sxs-lookup"><span data-stu-id="7d24e-142">NOTES</span></span>

## <span data-ttu-id="7d24e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d24e-143">RELATED LINKS</span></span>

