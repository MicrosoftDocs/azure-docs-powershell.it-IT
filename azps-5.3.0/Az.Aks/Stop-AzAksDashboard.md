---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475970"
---
# <span data-ttu-id="1adcb-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="1adcb-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="1adcb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1adcb-102">SYNOPSIS</span></span>
<span data-ttu-id="1adcb-103">Interrompi il tunnel di Kubectl SSH creato in Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="1adcb-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="1adcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1adcb-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1adcb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1adcb-105">DESCRIPTION</span></span>
<span data-ttu-id="1adcb-106">Interrompi il tunnel di Kubectl SSH creato in Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="1adcb-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="1adcb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1adcb-107">EXAMPLES</span></span>

### <span data-ttu-id="1adcb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1adcb-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="1adcb-109">Interrompe la configurazione del tunnel SSH esistente eseguendo Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="1adcb-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="1adcb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1adcb-110">PARAMETERS</span></span>

### <span data-ttu-id="1adcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1adcb-111">-DefaultProfile</span></span>
<span data-ttu-id="1adcb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1adcb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1adcb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1adcb-113">-PassThru</span></span>
<span data-ttu-id="1adcb-114">Restituisce vero se il tunnel SSH è chiuso.</span><span class="sxs-lookup"><span data-stu-id="1adcb-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="1adcb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adcb-115">CommonParameters</span></span>
<span data-ttu-id="1adcb-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1adcb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adcb-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1adcb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adcb-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1adcb-118">INPUTS</span></span>

### <span data-ttu-id="1adcb-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1adcb-119">None</span></span>

## <span data-ttu-id="1adcb-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1adcb-120">OUTPUTS</span></span>

### <span data-ttu-id="1adcb-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1adcb-121">System.Boolean</span></span>

## <span data-ttu-id="1adcb-122">Note</span><span class="sxs-lookup"><span data-stu-id="1adcb-122">NOTES</span></span>

## <span data-ttu-id="1adcb-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1adcb-123">RELATED LINKS</span></span>
