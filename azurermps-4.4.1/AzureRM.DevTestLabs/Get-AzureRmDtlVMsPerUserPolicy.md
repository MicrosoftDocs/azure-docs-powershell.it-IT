---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 2be26f222be7ec444706fb15fb862a43dc8b8116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520106"
---
# <span data-ttu-id="ecbe1-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="ecbe1-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="ecbe1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecbe1-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbe1-103">Ottiene i criteri per gli utenti delle macchine virtuali di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecbe1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecbe1-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecbe1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecbe1-105">DESCRIPTION</span></span>
<span data-ttu-id="ecbe1-106">Il cmdlet **Get-AzureRmDtlVMsPerUserPolicy** ottiene le macchine virtuali per i criteri utente di un Lab, che consente di impostare il numero massimo di macchine virtuali consentite per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="ecbe1-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero massimo di macchine virtuali consentite per ogni utente impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="ecbe1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecbe1-108">EXAMPLES</span></span>

## <span data-ttu-id="ecbe1-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecbe1-109">PARAMETERS</span></span>

### <span data-ttu-id="ecbe1-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="ecbe1-110">-LabName</span></span>
<span data-ttu-id="ecbe1-111">Specifica il nome del Lab per cui questo cmdlet ottiene il criterio per utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-111">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecbe1-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbe1-112">-ResourceGroupName</span></span>
<span data-ttu-id="ecbe1-113">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-113">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecbe1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbe1-114">-DefaultProfile</span></span>
<span data-ttu-id="ecbe1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecbe1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbe1-116">CommonParameters</span></span>
<span data-ttu-id="ecbe1-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbe1-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecbe1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbe1-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecbe1-119">INPUTS</span></span>

## <span data-ttu-id="ecbe1-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecbe1-120">OUTPUTS</span></span>

### <span data-ttu-id="ecbe1-121">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ecbe1-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="ecbe1-122">Questo cmdlet restituisce il criterio che specifica il numero massimo di macchine virtuali che possono essere create da un utente in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="ecbe1-122">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="ecbe1-123">Note</span><span class="sxs-lookup"><span data-stu-id="ecbe1-123">NOTES</span></span>

## <span data-ttu-id="ecbe1-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecbe1-124">RELATED LINKS</span></span>

[<span data-ttu-id="ecbe1-125">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="ecbe1-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)

