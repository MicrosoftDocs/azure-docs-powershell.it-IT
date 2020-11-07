---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686778"
---
# <span data-ttu-id="fe316-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="fe316-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="fe316-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe316-102">SYNOPSIS</span></span>
<span data-ttu-id="fe316-103">Rimuove un sito di ripristino del sito dall'archivio corrente.</span><span class="sxs-lookup"><span data-stu-id="fe316-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe316-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe316-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe316-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe316-105">DESCRIPTION</span></span>
<span data-ttu-id="fe316-106">Il cmdlet **Remove-AzureRmSiteRecoverySite** Elimina un sito di ripristino del sito di Azure dall'archivio corrente.</span><span class="sxs-lookup"><span data-stu-id="fe316-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="fe316-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe316-107">EXAMPLES</span></span>

## <span data-ttu-id="fe316-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe316-108">PARAMETERS</span></span>

### <span data-ttu-id="fe316-109">-Force</span><span class="sxs-lookup"><span data-stu-id="fe316-109">-Force</span></span>
<span data-ttu-id="fe316-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fe316-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe316-111">-Sito</span><span class="sxs-lookup"><span data-stu-id="fe316-111">-Site</span></span>
<span data-ttu-id="fe316-112">Specifica l'oggetto sito di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="fe316-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe316-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe316-113">-Confirm</span></span>
<span data-ttu-id="fe316-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe316-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe316-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe316-115">-WhatIf</span></span>
<span data-ttu-id="fe316-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe316-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fe316-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe316-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe316-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe316-118">-DefaultProfile</span></span>
<span data-ttu-id="fe316-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe316-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe316-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe316-120">CommonParameters</span></span>
<span data-ttu-id="fe316-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe316-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe316-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe316-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe316-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe316-123">INPUTS</span></span>

### <span data-ttu-id="fe316-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="fe316-124">ASRSite</span></span>
<span data-ttu-id="fe316-125">Il parametro "sito" accetta il valore di tipo "ASRSite" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe316-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="fe316-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe316-126">OUTPUTS</span></span>

## <span data-ttu-id="fe316-127">Note</span><span class="sxs-lookup"><span data-stu-id="fe316-127">NOTES</span></span>

## <span data-ttu-id="fe316-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe316-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe316-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="fe316-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="fe316-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="fe316-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
