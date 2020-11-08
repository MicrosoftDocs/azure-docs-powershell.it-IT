---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: c9427df1710ad7232cf66ce576cf2c3db409f7d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022248"
---
# <span data-ttu-id="3c233-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c233-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="3c233-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c233-102">SYNOPSIS</span></span>
<span data-ttu-id="3c233-103">Ottiene i criteri di sicurezza dei dati avanzati di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="3c233-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="3c233-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c233-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c233-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c233-105">DESCRIPTION</span></span>
<span data-ttu-id="3c233-106">Il cmdlet **Get-AzSqlInstanceAdvancedDataSecurityPolicy** recupera i criteri avanzati per la sicurezza dei dati di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="3c233-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="3c233-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c233-107">EXAMPLES</span></span>

### <span data-ttu-id="3c233-108">Esempio 1-Ottiene la sicurezza dei dati avanzata dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="3c233-108">Example 1 - Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="3c233-109">Esempio 2-ottiene la sicurezza avanzata dei dati dell'istanza gestita dalla risorsa istanza gestita</span><span class="sxs-lookup"><span data-stu-id="3c233-109">Example 2 - Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="3c233-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c233-110">PARAMETERS</span></span>

### <span data-ttu-id="3c233-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c233-111">-DefaultProfile</span></span>
<span data-ttu-id="3c233-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c233-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c233-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c233-113">-InputObject</span></span>
<span data-ttu-id="3c233-114">L'oggetto istanza gestita da usare con l'operazione Advanced Data Security Policy</span><span class="sxs-lookup"><span data-stu-id="3c233-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c233-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3c233-115">-InstanceName</span></span>
<span data-ttu-id="3c233-116">Nome dell'istanza gestita del database SQL.</span><span class="sxs-lookup"><span data-stu-id="3c233-116">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c233-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c233-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c233-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c233-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c233-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c233-119">CommonParameters</span></span>
<span data-ttu-id="3c233-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c233-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c233-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c233-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c233-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c233-122">INPUTS</span></span>

### <span data-ttu-id="3c233-123">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3c233-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="3c233-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3c233-124">System.String</span></span>

## <span data-ttu-id="3c233-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c233-125">OUTPUTS</span></span>

### <span data-ttu-id="3c233-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3c233-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="3c233-127">Note</span><span class="sxs-lookup"><span data-stu-id="3c233-127">NOTES</span></span>

## <span data-ttu-id="3c233-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c233-128">RELATED LINKS</span></span>
