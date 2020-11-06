---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519507"
---
# <span data-ttu-id="b7b8c-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b7b8c-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="b7b8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b8c-103">Crea un mapping del contenitore di protezione del ripristino di Azure site associando un criterio a un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7b8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7b8c-104">SYNTAX</span></span>

### <span data-ttu-id="b7b8c-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7b8c-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7b8c-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b7b8c-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b8c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7b8c-107">DESCRIPTION</span></span>
<span data-ttu-id="b7b8c-108">Il cmdlet **New-AzureRmSiteRecoveryProtectionContainerMapping** crea un mapping del contenitore di protezione del ripristino di Azure site associando un criterio a un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="b7b8c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7b8c-109">EXAMPLES</span></span>

## <span data-ttu-id="b7b8c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7b8c-110">PARAMETERS</span></span>

### <span data-ttu-id="b7b8c-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7b8c-111">-Name</span></span>
<span data-ttu-id="b7b8c-112">Specifica il nome del mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-112">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="b7b8c-113">-Policy</span><span class="sxs-lookup"><span data-stu-id="b7b8c-113">-Policy</span></span>
<span data-ttu-id="b7b8c-114">Specifica l'oggetto Criteri di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-114">Specifies the Azure Site Recovery Policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8c-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b7b8c-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="b7b8c-116">Specifica l'oggetto contenitore di protezione principale.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-116">Specifies the primary Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8c-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b7b8c-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="b7b8c-118">Specifica l'oggetto contenitore di protezione ripristino.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-118">Specifies the Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b8c-119">-DefaultProfile</span></span>
<span data-ttu-id="b7b8c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b8c-121">CommonParameters</span></span>
<span data-ttu-id="b7b8c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b8c-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b8c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b8c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7b8c-124">INPUTS</span></span>

### <span data-ttu-id="b7b8c-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b7b8c-125">ASRPolicy</span></span>
<span data-ttu-id="b7b8c-126">Il parametro ' Policy ' accetta il valore di tipo ' ASRPolicy ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b7b8c-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="b7b8c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7b8c-127">OUTPUTS</span></span>

### <span data-ttu-id="b7b8c-128">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b7b8c-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b7b8c-129">Note</span><span class="sxs-lookup"><span data-stu-id="b7b8c-129">NOTES</span></span>

## <span data-ttu-id="b7b8c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7b8c-130">RELATED LINKS</span></span>

[<span data-ttu-id="b7b8c-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b7b8c-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="b7b8c-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b7b8c-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
