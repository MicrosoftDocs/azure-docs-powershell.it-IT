---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: a83b4b8ca3dbe415013fe9a858d46cb886ce4b00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507952"
---
# <span data-ttu-id="559a6-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="559a6-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="559a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="559a6-102">SYNOPSIS</span></span>
<span data-ttu-id="559a6-103">Rimuove un sito di ripristino del sito dall'archivio corrente.</span><span class="sxs-lookup"><span data-stu-id="559a6-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="559a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="559a6-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="559a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="559a6-105">DESCRIPTION</span></span>
<span data-ttu-id="559a6-106">Il cmdlet **Remove-AzureRmSiteRecoverySite** Elimina un sito di ripristino del sito di Azure dall'archivio corrente.</span><span class="sxs-lookup"><span data-stu-id="559a6-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="559a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="559a6-107">EXAMPLES</span></span>

## <span data-ttu-id="559a6-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="559a6-108">PARAMETERS</span></span>

### <span data-ttu-id="559a6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559a6-109">-DefaultProfile</span></span>
<span data-ttu-id="559a6-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="559a6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="559a6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="559a6-111">-Force</span></span>
<span data-ttu-id="559a6-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="559a6-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559a6-113">-Sito</span><span class="sxs-lookup"><span data-stu-id="559a6-113">-Site</span></span>
<span data-ttu-id="559a6-114">Specifica l'oggetto sito di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="559a6-114">Specifies the Site Recovery site object.</span></span>

```yaml
Type: ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="559a6-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="559a6-115">-Confirm</span></span>
<span data-ttu-id="559a6-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="559a6-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559a6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="559a6-117">-WhatIf</span></span>
<span data-ttu-id="559a6-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="559a6-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="559a6-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="559a6-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559a6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559a6-120">CommonParameters</span></span>
<span data-ttu-id="559a6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="559a6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559a6-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="559a6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559a6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="559a6-123">INPUTS</span></span>

### <span data-ttu-id="559a6-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="559a6-124">ASRSite</span></span>
<span data-ttu-id="559a6-125">Il parametro "sito" accetta il valore di tipo "ASRSite" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="559a6-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="559a6-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="559a6-126">OUTPUTS</span></span>

## <span data-ttu-id="559a6-127">Note</span><span class="sxs-lookup"><span data-stu-id="559a6-127">NOTES</span></span>

## <span data-ttu-id="559a6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="559a6-128">RELATED LINKS</span></span>

[<span data-ttu-id="559a6-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="559a6-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="559a6-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="559a6-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
