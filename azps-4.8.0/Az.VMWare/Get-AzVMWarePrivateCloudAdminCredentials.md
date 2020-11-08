---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032778"
---
# <span data-ttu-id="368f0-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="368f0-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="368f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="368f0-102">SYNOPSIS</span></span>
<span data-ttu-id="368f0-103">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="368f0-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="368f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="368f0-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="368f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="368f0-105">DESCRIPTION</span></span>
<span data-ttu-id="368f0-106">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="368f0-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="368f0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="368f0-107">EXAMPLES</span></span>

### <span data-ttu-id="368f0-108">Esempio 1: ottenere le credenziali di amministratore di private cloud</span><span class="sxs-lookup"><span data-stu-id="368f0-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="368f0-109">Ottenere le credenziali di amministratore del cloud privato</span><span class="sxs-lookup"><span data-stu-id="368f0-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="368f0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="368f0-110">PARAMETERS</span></span>

### <span data-ttu-id="368f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368f0-111">-DefaultProfile</span></span>
<span data-ttu-id="368f0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="368f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="368f0-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="368f0-113">-PrivateCloudName</span></span>
<span data-ttu-id="368f0-114">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="368f0-114">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="368f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="368f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="368f0-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="368f0-116">The name of the resource group.</span></span>
<span data-ttu-id="368f0-117">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="368f0-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="368f0-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="368f0-118">-SubscriptionId</span></span>
<span data-ttu-id="368f0-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="368f0-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="368f0-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="368f0-120">-Confirm</span></span>
<span data-ttu-id="368f0-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="368f0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="368f0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="368f0-122">-WhatIf</span></span>
<span data-ttu-id="368f0-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="368f0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="368f0-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="368f0-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="368f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368f0-125">CommonParameters</span></span>
<span data-ttu-id="368f0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="368f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368f0-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="368f0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368f0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="368f0-128">INPUTS</span></span>

## <span data-ttu-id="368f0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="368f0-129">OUTPUTS</span></span>

### <span data-ttu-id="368f0-130">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="368f0-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="368f0-131">Note</span><span class="sxs-lookup"><span data-stu-id="368f0-131">NOTES</span></span>

<span data-ttu-id="368f0-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="368f0-132">ALIASES</span></span>

## <span data-ttu-id="368f0-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="368f0-133">RELATED LINKS</span></span>

