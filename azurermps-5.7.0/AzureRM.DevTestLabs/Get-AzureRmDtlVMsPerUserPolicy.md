---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 53afed94f9733c041df2c49ff1ec97a2fb8277f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512612"
---
# <span data-ttu-id="c9451-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c9451-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="c9451-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9451-102">SYNOPSIS</span></span>
<span data-ttu-id="c9451-103">Ottiene i criteri per gli utenti delle macchine virtuali di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="c9451-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9451-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9451-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9451-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9451-105">DESCRIPTION</span></span>
<span data-ttu-id="c9451-106">Il cmdlet **Get-AzureRmDtlVMsPerUserPolicy** ottiene le macchine virtuali per i criteri utente di un Lab, che consente di impostare il numero massimo di macchine virtuali consentite per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="c9451-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="c9451-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero massimo di macchine virtuali consentite per ogni utente impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="c9451-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="c9451-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9451-108">EXAMPLES</span></span>

## <span data-ttu-id="c9451-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9451-109">PARAMETERS</span></span>

### <span data-ttu-id="c9451-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9451-110">-DefaultProfile</span></span>
<span data-ttu-id="c9451-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c9451-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9451-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="c9451-112">-LabName</span></span>
<span data-ttu-id="c9451-113">Specifica il nome del Lab per cui questo cmdlet ottiene il criterio per utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9451-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9451-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9451-114">-ResourceGroupName</span></span>
<span data-ttu-id="c9451-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="c9451-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9451-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9451-116">CommonParameters</span></span>
<span data-ttu-id="c9451-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9451-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9451-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9451-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9451-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9451-119">INPUTS</span></span>

### <span data-ttu-id="c9451-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c9451-120">None</span></span>
<span data-ttu-id="c9451-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c9451-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9451-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9451-122">OUTPUTS</span></span>

### <span data-ttu-id="c9451-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c9451-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="c9451-124">Questo cmdlet restituisce il criterio che specifica il numero massimo di macchine virtuali che possono essere create da un utente in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="c9451-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="c9451-125">Note</span><span class="sxs-lookup"><span data-stu-id="c9451-125">NOTES</span></span>

## <span data-ttu-id="c9451-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9451-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9451-127">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c9451-127">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


