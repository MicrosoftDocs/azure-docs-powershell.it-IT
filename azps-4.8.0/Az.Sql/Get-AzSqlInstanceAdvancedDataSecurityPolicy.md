---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191215"
---
# <span data-ttu-id="603ad-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="603ad-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="603ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="603ad-102">SYNOPSIS</span></span>
<span data-ttu-id="603ad-103">Ottiene i criteri di sicurezza dei dati avanzati di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="603ad-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="603ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="603ad-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="603ad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="603ad-105">DESCRIPTION</span></span>
<span data-ttu-id="603ad-106">Il cmdlet **Get-AzSqlInstanceAdvancedDataSecurityPolicy** recupera i criteri avanzati per la sicurezza dei dati di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="603ad-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="603ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="603ad-107">EXAMPLES</span></span>

### <span data-ttu-id="603ad-108">Esempio 1: ottiene la sicurezza dei dati avanzata dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="603ad-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="603ad-109">Esempio 2: ottiene la sicurezza dei dati avanzata dell'istanza gestita dalla risorsa istanza gestita</span><span class="sxs-lookup"><span data-stu-id="603ad-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="603ad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="603ad-110">PARAMETERS</span></span>

### <span data-ttu-id="603ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="603ad-111">-DefaultProfile</span></span>
<span data-ttu-id="603ad-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="603ad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="603ad-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="603ad-113">-InputObject</span></span>
<span data-ttu-id="603ad-114">L'oggetto istanza gestita da usare con l'operazione Advanced Data Security Policy</span><span class="sxs-lookup"><span data-stu-id="603ad-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="603ad-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="603ad-115">-InstanceName</span></span>
<span data-ttu-id="603ad-116">Nome dell'istanza gestita del database SQL.</span><span class="sxs-lookup"><span data-stu-id="603ad-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="603ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="603ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="603ad-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="603ad-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="603ad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603ad-119">CommonParameters</span></span>
<span data-ttu-id="603ad-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="603ad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603ad-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="603ad-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603ad-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="603ad-122">INPUTS</span></span>

### <span data-ttu-id="603ad-123">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="603ad-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="603ad-124">System. String</span><span class="sxs-lookup"><span data-stu-id="603ad-124">System.String</span></span>

## <span data-ttu-id="603ad-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="603ad-125">OUTPUTS</span></span>

### <span data-ttu-id="603ad-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="603ad-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="603ad-127">Note</span><span class="sxs-lookup"><span data-stu-id="603ad-127">NOTES</span></span>

## <span data-ttu-id="603ad-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="603ad-128">RELATED LINKS</span></span>