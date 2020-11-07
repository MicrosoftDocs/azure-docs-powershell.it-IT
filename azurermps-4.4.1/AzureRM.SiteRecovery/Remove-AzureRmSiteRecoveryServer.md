---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688230"
---
# <span data-ttu-id="e270c-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e270c-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="e270c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e270c-102">SYNOPSIS</span></span>
<span data-ttu-id="e270c-103">Rimuove un server di ripristino del sito dall'archivio corrente.</span><span class="sxs-lookup"><span data-stu-id="e270c-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e270c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e270c-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e270c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e270c-105">DESCRIPTION</span></span>
<span data-ttu-id="e270c-106">Il cmdlet **Remove-AzureRmSiteRecoveryServer** Annulla la registrazione di un server di ripristino del sito di Azure che lo rimuove dalla volta corrente.</span><span class="sxs-lookup"><span data-stu-id="e270c-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="e270c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e270c-107">EXAMPLES</span></span>

## <span data-ttu-id="e270c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e270c-108">PARAMETERS</span></span>

### <span data-ttu-id="e270c-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e270c-109">-Force</span></span>
<span data-ttu-id="e270c-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e270c-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e270c-111">-Server</span><span class="sxs-lookup"><span data-stu-id="e270c-111">-Server</span></span>
<span data-ttu-id="e270c-112">Specifica l'oggetto server di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="e270c-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e270c-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e270c-113">-Confirm</span></span>
<span data-ttu-id="e270c-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e270c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e270c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e270c-115">-WhatIf</span></span>
<span data-ttu-id="e270c-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e270c-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e270c-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e270c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e270c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e270c-118">-DefaultProfile</span></span>
<span data-ttu-id="e270c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e270c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e270c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e270c-120">CommonParameters</span></span>
<span data-ttu-id="e270c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e270c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e270c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e270c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e270c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e270c-123">INPUTS</span></span>

### <span data-ttu-id="e270c-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="e270c-124">ASRServer</span></span>
<span data-ttu-id="e270c-125">Il parametro ' server ' accetta il valore di tipo ' ASRServer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e270c-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="e270c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e270c-126">OUTPUTS</span></span>

### <span data-ttu-id="e270c-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="e270c-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="e270c-128">Note</span><span class="sxs-lookup"><span data-stu-id="e270c-128">NOTES</span></span>

## <span data-ttu-id="e270c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e270c-129">RELATED LINKS</span></span>

[<span data-ttu-id="e270c-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e270c-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="e270c-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e270c-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
