---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 4ec1c8c2788469ffd377127bc58f657c817434a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519487"
---
# <span data-ttu-id="a5aad-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="a5aad-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="a5aad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5aad-102">SYNOPSIS</span></span>
<span data-ttu-id="a5aad-103">Interrompi il tunnel di Kubectl SSH creato in Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="a5aad-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5aad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5aad-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5aad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5aad-105">DESCRIPTION</span></span>
<span data-ttu-id="a5aad-106">Interrompi il tunnel di Kubectl SSH creato in Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="a5aad-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="a5aad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5aad-107">EXAMPLES</span></span>

### <span data-ttu-id="a5aad-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5aad-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="a5aad-109">Interrompe la configurazione del tunnel SSH esistente eseguendo Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="a5aad-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="a5aad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5aad-110">PARAMETERS</span></span>

### <span data-ttu-id="a5aad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5aad-111">-DefaultProfile</span></span>
<span data-ttu-id="a5aad-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5aad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5aad-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5aad-113">-PassThru</span></span>
<span data-ttu-id="a5aad-114">Restituisce vero se il tunnel SSH è chiuso.</span><span class="sxs-lookup"><span data-stu-id="a5aad-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="a5aad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5aad-115">CommonParameters</span></span>
<span data-ttu-id="a5aad-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5aad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5aad-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5aad-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5aad-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5aad-118">INPUTS</span></span>

### <span data-ttu-id="a5aad-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5aad-119">None</span></span>

## <span data-ttu-id="a5aad-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5aad-120">OUTPUTS</span></span>

### <span data-ttu-id="a5aad-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5aad-121">System.Boolean</span></span>

## <span data-ttu-id="a5aad-122">Note</span><span class="sxs-lookup"><span data-stu-id="a5aad-122">NOTES</span></span>

## <span data-ttu-id="a5aad-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5aad-123">RELATED LINKS</span></span>
