---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520356"
---
# <span data-ttu-id="c4e45-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="c4e45-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="c4e45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4e45-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e45-103">Ottiene informazioni sulle macchine virtuali gestite dal ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="c4e45-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4e45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4e45-104">SYNTAX</span></span>

### <span data-ttu-id="c4e45-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4e45-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4e45-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c4e45-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4e45-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c4e45-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4e45-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4e45-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e45-109">Il cmdlet **Get-AzureRmSiteRecoveryVM** ottiene informazioni sulle macchine virtuali gestite in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c4e45-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="c4e45-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4e45-110">EXAMPLES</span></span>

## <span data-ttu-id="c4e45-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4e45-111">PARAMETERS</span></span>

### <span data-ttu-id="c4e45-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e45-112">-DefaultProfile</span></span>
<span data-ttu-id="c4e45-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e45-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4e45-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c4e45-114">-FriendlyName</span></span>
<span data-ttu-id="c4e45-115">Specifica il nome descrittivo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4e45-115">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e45-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4e45-116">-Name</span></span>
<span data-ttu-id="c4e45-117">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4e45-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e45-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c4e45-118">-ProtectionContainer</span></span>
<span data-ttu-id="c4e45-119">Specifica l'oggetto contenitore di protezione per il ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="c4e45-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e45-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e45-120">CommonParameters</span></span>
<span data-ttu-id="c4e45-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e45-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e45-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e45-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e45-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4e45-123">INPUTS</span></span>

### <span data-ttu-id="c4e45-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c4e45-124">ASRProtectionContainer</span></span>
<span data-ttu-id="c4e45-125">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c4e45-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="c4e45-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c4e45-126">ASRProtectionContainer</span></span>
<span data-ttu-id="c4e45-127">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c4e45-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="c4e45-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4e45-128">OUTPUTS</span></span>

### <span data-ttu-id="c4e45-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="c4e45-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="c4e45-130">Note</span><span class="sxs-lookup"><span data-stu-id="c4e45-130">NOTES</span></span>

## <span data-ttu-id="c4e45-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4e45-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4e45-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="c4e45-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)