---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474812"
---
# <span data-ttu-id="f112c-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="f112c-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="f112c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f112c-102">SYNOPSIS</span></span>
<span data-ttu-id="f112c-103">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="f112c-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="f112c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f112c-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f112c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f112c-105">DESCRIPTION</span></span>
<span data-ttu-id="f112c-106">Elencare le credenziali di amministratore per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="f112c-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="f112c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f112c-107">EXAMPLES</span></span>

### <span data-ttu-id="f112c-108">Esempio 1: ottenere le credenziali di amministratore di private cloud</span><span class="sxs-lookup"><span data-stu-id="f112c-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="f112c-109">Ottenere le credenziali di amministratore del cloud privato</span><span class="sxs-lookup"><span data-stu-id="f112c-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="f112c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f112c-110">PARAMETERS</span></span>

### <span data-ttu-id="f112c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f112c-111">-DefaultProfile</span></span>
<span data-ttu-id="f112c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f112c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f112c-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f112c-113">-PrivateCloudName</span></span>
<span data-ttu-id="f112c-114">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="f112c-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="f112c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f112c-115">-ResourceGroupName</span></span>
<span data-ttu-id="f112c-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f112c-116">The name of the resource group.</span></span>
<span data-ttu-id="f112c-117">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f112c-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f112c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f112c-118">-SubscriptionId</span></span>
<span data-ttu-id="f112c-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f112c-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f112c-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f112c-120">-Confirm</span></span>
<span data-ttu-id="f112c-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f112c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f112c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f112c-122">-WhatIf</span></span>
<span data-ttu-id="f112c-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f112c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f112c-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f112c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f112c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f112c-125">CommonParameters</span></span>
<span data-ttu-id="f112c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f112c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f112c-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f112c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f112c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f112c-128">INPUTS</span></span>

## <span data-ttu-id="f112c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f112c-129">OUTPUTS</span></span>

### <span data-ttu-id="f112c-130">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="f112c-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="f112c-131">Note</span><span class="sxs-lookup"><span data-stu-id="f112c-131">NOTES</span></span>

<span data-ttu-id="f112c-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f112c-132">ALIASES</span></span>

## <span data-ttu-id="f112c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f112c-133">RELATED LINKS</span></span>

