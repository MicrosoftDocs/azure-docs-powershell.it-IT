---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861710"
---
# <span data-ttu-id="79ccf-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="79ccf-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="79ccf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="79ccf-103">Ottenere un elenco di tutti gli oggetti quota per il Vault in una posizione.</span><span class="sxs-lookup"><span data-stu-id="79ccf-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="79ccf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79ccf-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="79ccf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="79ccf-106">Ottenere un elenco di tutti gli oggetti quota per il Vault in una posizione.</span><span class="sxs-lookup"><span data-stu-id="79ccf-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="79ccf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79ccf-107">EXAMPLES</span></span>

### <span data-ttu-id="79ccf-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="79ccf-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="79ccf-109">Ottenere un elenco di tutti gli oggetti quota per il Vault in una posizione.</span><span class="sxs-lookup"><span data-stu-id="79ccf-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="79ccf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79ccf-110">PARAMETERS</span></span>

### <span data-ttu-id="79ccf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ccf-111">-DefaultProfile</span></span>
<span data-ttu-id="79ccf-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79ccf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="79ccf-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="79ccf-113">-Location</span></span>
<span data-ttu-id="79ccf-114">Posizione della quota.</span><span class="sxs-lookup"><span data-stu-id="79ccf-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="79ccf-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79ccf-115">-SubscriptionId</span></span>
<span data-ttu-id="79ccf-116">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="79ccf-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="79ccf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ccf-117">CommonParameters</span></span>
<span data-ttu-id="79ccf-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ccf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ccf-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79ccf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ccf-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79ccf-120">INPUTS</span></span>

## <span data-ttu-id="79ccf-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79ccf-121">OUTPUTS</span></span>

### <span data-ttu-id="79ccf-122">Microsoft. Azure. PowerShell. Cmdlets. KeyVaultAdmin. Models. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="79ccf-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="79ccf-123">Note</span><span class="sxs-lookup"><span data-stu-id="79ccf-123">NOTES</span></span>

## <span data-ttu-id="79ccf-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79ccf-124">RELATED LINKS</span></span>

