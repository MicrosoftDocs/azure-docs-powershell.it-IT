---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192639"
---
# <span data-ttu-id="24912-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="24912-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="24912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24912-102">SYNOPSIS</span></span>
<span data-ttu-id="24912-103">Interrompere il tunnel Kubectl SSH creato in Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="24912-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="24912-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24912-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24912-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="24912-105">DESCRIPTION</span></span>
<span data-ttu-id="24912-106">Interrompere il tunnel Kubectl SSH creato in Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="24912-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="24912-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24912-107">EXAMPLES</span></span>

### <span data-ttu-id="24912-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24912-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="24912-109">Interrompe l'installazione esistente dei tunnel SSH eseguendo Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="24912-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="24912-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24912-110">PARAMETERS</span></span>

### <span data-ttu-id="24912-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24912-111">-DefaultProfile</span></span>
<span data-ttu-id="24912-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24912-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24912-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24912-113">-PassThru</span></span>
<span data-ttu-id="24912-114">Restituisce true se il tunnel SSH è chiuso.</span><span class="sxs-lookup"><span data-stu-id="24912-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="24912-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24912-115">CommonParameters</span></span>
<span data-ttu-id="24912-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24912-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24912-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24912-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24912-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="24912-118">INPUTS</span></span>

### <span data-ttu-id="24912-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="24912-119">None</span></span>

## <span data-ttu-id="24912-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24912-120">OUTPUTS</span></span>

### <span data-ttu-id="24912-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24912-121">System.Boolean</span></span>

## <span data-ttu-id="24912-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="24912-122">NOTES</span></span>

## <span data-ttu-id="24912-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24912-123">RELATED LINKS</span></span>
