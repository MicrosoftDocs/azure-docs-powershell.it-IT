---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 3a3106dc400345b3debddc54cc9a9f8fdfd8f816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678905"
---
# <span data-ttu-id="b64b7-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="b64b7-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="b64b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b64b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b64b7-103">Ottiene i criteri per gli utenti delle macchine virtuali di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="b64b7-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="b64b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b64b7-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b64b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b64b7-105">DESCRIPTION</span></span>
<span data-ttu-id="b64b7-106">Il cmdlet **Get-AzDtlVMsPerUserPolicy** ottiene le macchine virtuali per i criteri utente di un Lab, che consente di impostare il numero massimo di macchine virtuali consentite per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="b64b7-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="b64b7-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero massimo di macchine virtuali consentite per ogni utente impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="b64b7-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="b64b7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b64b7-108">EXAMPLES</span></span>

## <span data-ttu-id="b64b7-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b64b7-109">PARAMETERS</span></span>

### <span data-ttu-id="b64b7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64b7-110">-DefaultProfile</span></span>
<span data-ttu-id="b64b7-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b64b7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b64b7-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b64b7-112">-LabName</span></span>
<span data-ttu-id="b64b7-113">Specifica il nome del Lab per cui questo cmdlet ottiene il criterio per utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b64b7-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="b64b7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b64b7-114">-ResourceGroupName</span></span>
<span data-ttu-id="b64b7-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="b64b7-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b64b7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64b7-116">CommonParameters</span></span>
<span data-ttu-id="b64b7-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b64b7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64b7-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b64b7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64b7-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b64b7-119">INPUTS</span></span>

### <span data-ttu-id="b64b7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b64b7-120">System.String</span></span>

## <span data-ttu-id="b64b7-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b64b7-121">OUTPUTS</span></span>

### <span data-ttu-id="b64b7-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b64b7-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="b64b7-123">Note</span><span class="sxs-lookup"><span data-stu-id="b64b7-123">NOTES</span></span>

## <span data-ttu-id="b64b7-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b64b7-124">RELATED LINKS</span></span>

[<span data-ttu-id="b64b7-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="b64b7-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


