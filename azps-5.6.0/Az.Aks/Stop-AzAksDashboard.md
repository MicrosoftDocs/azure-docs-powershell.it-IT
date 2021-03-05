---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 633173a0ce8814ee2af9300be5b1cfc19bdf9a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975630"
---
# <span data-ttu-id="b4ae2-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="b4ae2-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="b4ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ae2-103">Interrompere il tunnel Kubectl SSH creato in Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="b4ae2-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="b4ae2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4ae2-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4ae2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ae2-106">Interrompere il tunnel Kubectl SSH creato in Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="b4ae2-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="b4ae2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4ae2-107">EXAMPLES</span></span>

### <span data-ttu-id="b4ae2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b4ae2-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="b4ae2-109">Interrompe la configurazione del tunnel SSH esistente eseguendo Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="b4ae2-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="b4ae2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ae2-110">PARAMETERS</span></span>

### <span data-ttu-id="b4ae2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ae2-111">-DefaultProfile</span></span>
<span data-ttu-id="b4ae2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ae2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ae2-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ae2-113">-PassThru</span></span>
<span data-ttu-id="b4ae2-114">Restituisce true se il tunnel SSH è chiuso.</span><span class="sxs-lookup"><span data-stu-id="b4ae2-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="b4ae2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ae2-115">CommonParameters</span></span>
<span data-ttu-id="b4ae2-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ae2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ae2-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4ae2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ae2-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4ae2-118">INPUTS</span></span>

### <span data-ttu-id="b4ae2-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b4ae2-119">None</span></span>

## <span data-ttu-id="b4ae2-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4ae2-120">OUTPUTS</span></span>

### <span data-ttu-id="b4ae2-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4ae2-121">System.Boolean</span></span>

## <span data-ttu-id="b4ae2-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4ae2-122">NOTES</span></span>

## <span data-ttu-id="b4ae2-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4ae2-123">RELATED LINKS</span></span>
